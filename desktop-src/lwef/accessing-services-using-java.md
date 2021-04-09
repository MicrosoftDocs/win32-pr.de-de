---
title: Zugreifen auf Dienste mithilfe von Java
description: Zugreifen auf Dienste mithilfe von Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948647"
---
# <a name="accessing-services-using-java"></a><span data-ttu-id="20bbf-103">Zugreifen auf Dienste mithilfe von Java</span><span class="sxs-lookup"><span data-stu-id="20bbf-103">Accessing Services Using Java</span></span>

<span data-ttu-id="20bbf-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="20bbf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="20bbf-105">Sie können auch von einem Java-Applet aus auf die Microsoft-Agent-Dienste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="20bbf-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="20bbf-106">Viele der Funktionen, auf die über die Microsoft-Agent-Schnittstellen zugegriffen werden kann, geben Werte durch Parameter als Verweis an</span><span class="sxs-lookup"><span data-stu-id="20bbf-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="20bbf-107">Um diese Parameter aus Java zu übergeben, müssen Arrays mit einem Element im Code erstellt und als Parameter an die entsprechende Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="20bbf-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="20bbf-108">Wenn Sie Microsoft Visual J++ verwenden und den Assistenten für die Java-Typbibliothek auf dem Microsoft-Agent-Server ausführen, lesen Sie die summary.txt-Datei, um zu überprüfen, welche Funktionen Array Argumente erfordern.</span><span class="sxs-lookup"><span data-stu-id="20bbf-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="20bbf-109">Die Vorgehensweise ähnelt der Vorgehensweise in C; Verwenden Sie die [**iagentex**](https://www.bing.com/search?q=**IAgentEx**) -Schnittstelle, um eine Instanz des Servers zu erstellen, und laden Sie dann das Zeichen:</span><span class="sxs-lookup"><span data-stu-id="20bbf-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



<span data-ttu-id="20bbf-110">Das Verfahren unterscheidet sich geringfügig beim Laden von Zeichen von einem http-Remote Speicherort wie einer Website.</span><span class="sxs-lookup"><span data-stu-id="20bbf-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="20bbf-111">In diesem Fall ist die [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) -Methode asynchron und auslöst eine com-Ausnahme von E \_ Pending (0x8000000a).</span><span class="sxs-lookup"><span data-stu-id="20bbf-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="20bbf-112">Sie müssen diese Ausnahme abfangen und ordnungsgemäß behandeln, wie dies in den folgenden Funktionen geschieht:</span><span class="sxs-lookup"><span data-stu-id="20bbf-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



<span data-ttu-id="20bbf-113">Dann erhalten Sie die [**iagentcharakteriex**](https://www.bing.com/search?q=**IAgentCharacterEx**) -Schnittstelle, die Ihnen den Zugriff auf die Methoden ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="20bbf-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="20bbf-114">Um über Ereignisse benachrichtigt zu werden, müssen Sie entweder die [**iagentnotifysink**](https://www.bing.com/search?q=**IAgentNotifySink**) -oder die [**iagentnotifysinkex**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) -Schnittstelle implementieren, um ein Objekt dieses Typs zu erstellen und zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="20bbf-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



<span data-ttu-id="20bbf-115">Um von einem Java-Applet aus auf den Microsoft-Agent zuzugreifen, müssen Sie Java-Klassen generieren, die Sie mit dem Applet installieren.</span><span class="sxs-lookup"><span data-stu-id="20bbf-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="20bbf-116">Sie können z. b. den Assistenten für die Visual J++-Java-Typbibliothek verwenden, um diese Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="20bbf-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="20bbf-117">Wenn Sie beabsichtigen, das Applet auf einer Webseite zu hosten, müssen Sie ein signiertes Java-CAB einschließlich der generierten Klassendateien erstellen, die mit der Seite heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="20bbf-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="20bbf-118">Die Klassendateien sind erforderlich, um auf den Microsoft-Agent-Server zuzugreifen, da es sich um ein COM-Objekt handelt, das außerhalb der Java Sandbox ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20bbf-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="20bbf-119">Weitere Informationen zur Trust-Based Sicherheit für Java finden Sie unter <https://www.microsoft.com/java/security> .</span><span class="sxs-lookup"><span data-stu-id="20bbf-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 