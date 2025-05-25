        import React, { useState } from 'react';

        function App() {
          // State for the contact form
          const [formData, setFormData] = useState({
            name: '',
            email: '',
            message: '',
          });

          const handleChange = (e) => {
            const { name, value } = e.target;
            setFormData((prevData) => ({
              ...prevData,
              [name]: value,
            }));
          };

          const handleSubmit = (e) => {
            e.preventDefault();
            console.log('Form submitted:', formData);
            alert('Thank you for your inquiry! We will get back to you soon at beachcitiescustomreels@gmail.com.');
            setFormData({
              name: '',
              email: '',
              message: '',
            });
          };

          return (
            // Main container with a background mimicking the flyer's subtle pattern/gradient
            <div className="min-h-screen p-4 sm:p-6 md:p-8 flex items-center justify-center font-sans"
                 style={{
                   background: 'linear-gradient(135deg, #FFDDC1, #FFECB3, #C8E6C9, #BBDEFB)', // Faded background colors
                   fontFamily: 'system-ui, -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji"', // Generic sans-serif
                 }}>
              {/* IMPORTANT: For local development, this script should ideally be in public/index.html */}
              {/* For immediate testing within a single file or certain sandboxes, placing it here can work */}
              <script src="https://cdn.tailwindcss.com"></script> 

              {/* Main content box resembling the flyer's central panel */}
              <div className="bg-yellow-50 p-6 sm:p-8 md:p-10 lg:p-12 rounded-3xl shadow-xl border-4 border-yellow-300 max-w-3xl w-full mx-auto text-center relative overflow-hidden">

                {/* Diagonal stripes on the top-right corner (mimicking flyer) */}
                <div className="absolute top-0 right-0 w-32 h-32 overflow-hidden">
                  <div className="absolute w-full h-full transform rotate-45 origin-bottom-left"
                       style={{
                         background: 'linear-gradient(to right, #FF7043 25%, transparent 25%, transparent 50%, #FF7043 50%, #FF7043 75%, transparent 75%, transparent 100%)',
                         backgroundSize: '20px 20px',
                         top: '-50%',
                         right: '-50%',
                         width: '200%',
                         height: '200%'
                       }}>
                  </div>
                </div>
                {/* Diagonal stripes on the bottom-left corner (mimicking flyer) */}
                <div className="absolute bottom-0 left-0 w-32 h-32 overflow-hidden">
                  <div className="absolute w-full h-full transform -rotate-135 origin-top-right"
                       style={{
                         background: 'linear-gradient(to right, #FF7043 25%, transparent 25%, transparent 50%, #FF7043 50%, #FF7043 75%, transparent 75%, transparent 100%)',
                         backgroundSize: '20px 20px',
                         bottom: '-50%',
                         left: '-50%',
                         width: '200%',
                         height: '200%'
                       }}>
                  </div>
                </div>

                {/* Main Content */}
                <div className="relative z-10">
                  <h1 className="text-4xl sm:text-5xl md:text-6xl font-extrabold text-orange-700 leading-tight mb-4 tracking-tight">
                    BEACH CITIES CUSTOM REELS
                  </h1>
                  <p className="text-xl sm:text-2xl font-bold text-red-600 mb-4">
                    Your Reel. Your Roles. Your Break.
                  </p>
                  <p className="text-lg sm:text-xl font-bold text-red-600 mb-8">
                    Ready to Book More Auditions?
                  </p>
                  <p className="text-base sm:text-lg text-gray-800 leading-relaxed mb-10 max-w-xl mx-auto">
                    Upgrade your acting reel with a professionally shot custom scene - written, filmed, and edited for you!
                  </p>

                  {/* WHAT YOU GET Section */}
                  <div className="bg-white p-6 sm:p-8 rounded-xl shadow-md border-2 border-orange-200 mb-10">
                    <h3 className="text-3xl font-extrabold text-orange-700 mb-6">WHAT YOU GET:</h3>
                    <ul className="list-none space-y-4 text-left text-lg sm:text-xl text-gray-800">
                      <li className="flex items-start">
                        <span className="text-green-500 mr-3 text-2xl">•</span>
                        <span>Custom script tailored to your type & genre (comedy, drama, thriller, etc.)</span>
                      </li>
                      <li className="flex items-start">
                        <span className="text-green-500 mr-3 text-2xl">•</span>
                        <span>Full production filmed in 4K with a professional cinema camera</span>
                      </li>
                      <li className="flex items-start">
                        <span className="text-green-500 mr-3 text-2xl">•</span>
                        <span>Direction & coaching from experienced filmmakers</span>
                      </li>
                    </ul>
                  </div>

                  {/* Intro Rate */}
                  <div className="mb-10">
                    <p className="text-3xl sm:text-4xl font-extrabold text-orange-700 mb-2">Intro Rate: $600</p>
                    <p className="text-lg text-gray-700">Final quote provided after free consultation</p>
                  </div>

                  {/* Location and Booking */}
                  <div className="mb-10 space-y-4">
                    <p className="flex items-center justify-center text-xl sm:text-2xl font-bold text-gray-800">
                      <span className="mr-3 text-blue-500 text-3xl">📍</span>
                      Serving the Beach Cities & Greater LA area
                    </p>
                    <p className="flex items-center justify-center text-xl sm:text-2xl font-bold text-gray-800">
                      <span className="mr-3 text-red-500 text-3xl">🗓️</span>
                      Limited bookings each month – reserve your shoot today!
                    </p>
                  </div>

                  {/* Meet the Directors Section */}
                  <div className="bg-white p-6 sm:p-8 rounded-xl shadow-md border-2 border-purple-200 mb-10 text-left">
                    <h3 className="text-3xl font-extrabold text-purple-700 mb-6 text-center">Meet the Directors: Frick & Frack</h3>
                    <p className="text-gray-700 leading-relaxed mb-4">
                      Frick & Frack is the brainchild of Joe Laporte and David Liehn, a powerhouse directing duo with a shared brain and a deep love for storytelling (and probably craft services). They first crossed paths on set back in 2019, and the creative sparks have been flying ever since.
                    </p>
                    <p className="text-gray-700 leading-relaxed mb-4">
                      Together, they’ve directed and produced everything from award-winning short films to music videos, web series, and commercials that actually make you want to watch commercials. As seasoned members of the Director’s Guild of America, Dave & Joe have clocked over 30 years in Hollywood, mostly wrangling chaos on big-budget TV ads as DGA Assistant Directors.
                    </p>
                    <p className="text-gray-700 leading-relaxed">
                      They got their start scaring audiences with horror, but these days, they’re all about the laughs. Comedy has become their playground and they’re not just playing. Their latest antics include launching the sketch-packed social channel Simple Goose Comedy, and dropping a brand-new YouTube series, Bagels & Banter, that’s basically brunch with a punchline.
                    </p>
                    <p className="text-gray-700 leading-relaxed mt-4 text-center font-semibold">
                      Frick & Frack: Two heads, one vision, and way too many inside jokes.
                    </p>
                  </div>

                  {/* Contact Information */}
                  <div className="space-y-4 mb-10">
                    <p className="flex items-center justify-center text-xl sm:text-2xl text-gray-800 font-bold">
                      <span className="mr-3 text-indigo-500 text-3xl">🌐</span>
                      Check out our work: <a href="http://fricknfrack.net" target="_blank" rel="noopener noreferrer" className="text-blue-600 hover:underline">fricknfrack.net</a>
                    </p>
                    <p className="flex items-center justify-center text-xl sm:text-2xl text-gray-800 font-bold">
                      <span className="mr-3 text-red-500 text-3xl">✉️</span>
                      Email: <a href="mailto:beachcitiescustomreels@gmail.com" className="text-blue-600 hover:underline">beachcitiescustomreels@gmail.com</a>
                    </p>
                  </div>

                  {/* Contact Form - Styled to fit flyer aesthetic */}
                  <div className="bg-white p-6 sm:p-8 rounded-xl shadow-md border-2 border-orange-200">
                    <h3 className="text-3xl font-extrabold text-orange-700 mb-8">Ready to Book?</h3>
                    <form onSubmit={handleSubmit} className="max-w-xl mx-auto space-y-6 text-left">
                      <div>
                        <label htmlFor="name" className="block text-gray-700 text-sm font-bold mb-2">
                          Name
                        </label>
                        <input
                          type="text"
                          id="name"
                          name="name"
                          value={formData.name}
                          onChange={handleChange}
                          className="shadow-sm appearance-none border rounded-lg w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                          required
                        />
                      </div>
                      <div>
                        <label htmlFor="email" className="block text-gray-700 text-sm font-bold mb-2">
                          Email
                        </label>
                        <input
                          type="email"
                          id="email"
                          name="email"
                          value={formData.email}
                          onChange={handleChange}
                          className="shadow-sm appearance-none border rounded-lg w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                          required
                        />
                      </div>
                      <div>
                        <label htmlFor="message" className="block text-gray-700 text-sm font-bold mb-2">
                          Your Message (e.g., "I'm interested in a 30-second reel!")
                        </label>
                        <textarea
                          id="message"
                          name="message"
                          value={formData.message}
                          onChange={handleChange}
                          rows="5"
                          className="shadow-sm appearance-none border rounded-lg w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                          required
                        ></textarea>
                      </div>
                      <div className="text-center">
                        <button
                          type="submit"
                          className="bg-orange-600 hover:bg-orange-700 text-white font-bold py-3 px-8 rounded-full text-lg shadow-lg transform hover:scale-105 transition duration-300 ease-in-out focus:outline-none focus:ring-4 focus:ring-orange-300"
                        >
                          Send Inquiry
                        </button>
                      </div>
                    </form>
                  </div>
                </div>
              </div>
            </div>
          );
        }

        export default App;
        
