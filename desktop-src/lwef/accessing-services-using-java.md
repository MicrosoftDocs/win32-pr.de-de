---
title: Zugreifen auf Dienste mit Java
description: Zugreifen auf Dienste mit Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a9a3feb1e6cb5fc9ddb8a24b87adfdb42461ebb4581723c1cdb465739c51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976850"
---
# <a name="accessing-services-using-java"></a>Zugreifen auf Dienste mit Java

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Sie können auch über ein Java-Applet auf Microsoft-Agent-Dienste zugreifen. Viele der Funktionen, auf die über die Microsoft Agent-Schnittstellen zugegriffen werden kann, geben Werte über Parameter zurück, die als Verweis übergeben werden. Um diese Parameter aus Java zu übergeben, ist es erforderlich, Einelementarrays in Ihrem Code zu erstellen und sie als Parameter an die entsprechende Funktion zu übergeben. Wenn Sie Microsoft Visual J++ verwenden und den Java-Typbibliotheks-Assistenten auf dem Microsoft-Agent-Server ausgeführt haben, lesen Sie die summary.txt-Datei, um zu überprüfen, welche Funktionen Arrayargumente erfordern. Die Prozedur ähnelt der in C. Sie verwenden die [**IAgentEx-Schnittstelle,**](https://www.bing.com/search?q=**IAgentEx**) um eine Instanz des Servers zu erstellen und dann das Zeichen zu laden:


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



Das Verfahren unterscheidet sich geringfügig, wenn Zeichen von einem HTTP-Remotespeicherort wie einer Website geladen werden. In diesem Fall ist die [**Load-Methode**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) asynchron und gibt eine COM-Ausnahme von E \_ PENDING (0x8000000a) aus. Sie müssen diese Ausnahme abfangen und ordnungsgemäß behandeln, wie dies in den folgenden Funktionen der Fall ist:


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



Anschließend erhalten Sie die [**IAgentCharacterEx-Schnittstelle,**](https://www.bing.com/search?q=**IAgentCharacterEx**) mit der Sie auf ihre Methoden zugreifen können:


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



Auf ähnliche Weise müssen Sie entweder die [**IAgentNotifySink-**](https://www.bing.com/search?q=**IAgentNotifySink**) oder die [**IAgentNotifySinkEx-Schnittstelle**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) implementieren, um über Ereignisse benachrichtigt zu werden, und ein Objekt dieses Typs erstellen und registrieren:


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



Um über ein Java-Applet auf den Microsoft-Agent zuzugreifen, müssen Sie Java-Klassen generieren, die Sie mit dem Applet installieren. Sie können z. B. den Visual J++-Java-Typbibliotheks-Assistenten verwenden, um diese Dateien zu generieren. Wenn Sie planen, das Applet auf einer Webseite zu hosten, müssen Sie ein signiertes Java CAB erstellen, das die generierten Klassendateien enthält, die mit der Seite heruntergeladen werden. Die Klassendateien sind für den Zugriff auf den Microsoft-Agent-Server erforderlich, da es sich um ein COM-Objekt handelt, das außerhalb der Java-Sandbox ausgeführt wird. Weitere Informationen zu Trust-Based Security for Java finden Sie unter <https://www.microsoft.com/java/security> .

 

 