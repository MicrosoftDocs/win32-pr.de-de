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
# <a name="accessing-services-using-java"></a>Zugreifen auf Dienste mithilfe von Java

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Sie können auch von einem Java-Applet aus auf die Microsoft-Agent-Dienste zugreifen. Viele der Funktionen, auf die über die Microsoft-Agent-Schnittstellen zugegriffen werden kann, geben Werte durch Parameter als Verweis an Um diese Parameter aus Java zu übergeben, müssen Arrays mit einem Element im Code erstellt und als Parameter an die entsprechende Funktion übergeben werden. Wenn Sie Microsoft Visual J++ verwenden und den Assistenten für die Java-Typbibliothek auf dem Microsoft-Agent-Server ausführen, lesen Sie die summary.txt-Datei, um zu überprüfen, welche Funktionen Array Argumente erfordern. Die Vorgehensweise ähnelt der Vorgehensweise in C; Verwenden Sie die [**iagentex**](https://www.bing.com/search?q=**IAgentEx**) -Schnittstelle, um eine Instanz des Servers zu erstellen, und laden Sie dann das Zeichen:


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



Das Verfahren unterscheidet sich geringfügig beim Laden von Zeichen von einem http-Remote Speicherort wie einer Website. In diesem Fall ist die [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) -Methode asynchron und auslöst eine com-Ausnahme von E \_ Pending (0x8000000a). Sie müssen diese Ausnahme abfangen und ordnungsgemäß behandeln, wie dies in den folgenden Funktionen geschieht:


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



Dann erhalten Sie die [**iagentcharakteriex**](https://www.bing.com/search?q=**IAgentCharacterEx**) -Schnittstelle, die Ihnen den Zugriff auf die Methoden ermöglicht:


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



Um über Ereignisse benachrichtigt zu werden, müssen Sie entweder die [**iagentnotifysink**](https://www.bing.com/search?q=**IAgentNotifySink**) -oder die [**iagentnotifysinkex**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) -Schnittstelle implementieren, um ein Objekt dieses Typs zu erstellen und zu registrieren:


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



Um von einem Java-Applet aus auf den Microsoft-Agent zuzugreifen, müssen Sie Java-Klassen generieren, die Sie mit dem Applet installieren. Sie können z. b. den Assistenten für die Visual J++-Java-Typbibliothek verwenden, um diese Dateien zu generieren. Wenn Sie beabsichtigen, das Applet auf einer Webseite zu hosten, müssen Sie ein signiertes Java-CAB einschließlich der generierten Klassendateien erstellen, die mit der Seite heruntergeladen werden. Die Klassendateien sind erforderlich, um auf den Microsoft-Agent-Server zuzugreifen, da es sich um ein COM-Objekt handelt, das außerhalb der Java Sandbox ausgeführt wird. Weitere Informationen zur Trust-Based Sicherheit für Java finden Sie unter <https://www.microsoft.com/java/security> .

 

 