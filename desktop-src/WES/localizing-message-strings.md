---
title: Lokalisieren von Meldungs Zeichenfolgen
description: Jede Nachrichten Zeichenfolge, die Sie im Manifest angeben, muss im Lokalisierungs Abschnitt des Manifests auf eine Zeichenfolge verweisen.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039291"
---
# <a name="localizing-message-strings"></a>Lokalisieren von Meldungs Zeichenfolgen

Jede Nachrichten Zeichenfolge, die Sie im Manifest angeben, muss im **Lokalisierungs** Abschnitt des Manifests auf eine Zeichenfolge verweisen. Der Abschnitt Lokalisierung enthält einen Zeichen folgen Tabellen Abschnitt für jedes Gebiets Schema, das Sie unterstützen.

Im folgenden Beispiel wird gezeigt, wie eine Zeichen folgen Tabelle definiert wird. Sie müssen die Attribute **ID** und **value** der Zeichenfolge angeben. Sie verwenden den Wert des **ID** -Attributs, um auf die Zeichenfolge im Manifest zu verweisen. Das **value** -Attribut enthält die lokalisierte Zeichenfolge.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


Anstatt dem Manifest lokalisierte Zeichen folgen hinzuzufügen, sollten Sie eine MUI-Datei (mehrsprachige Benutzeroberfläche) für jede Sprache erstellen, die Sie unterstützen. Verwenden Sie eine Meldungs Textdatei, um die lokalisierten Zeichen folgen anzugeben.

Im folgenden Verfahren wird beschrieben, wie eine MUI-Datei für Englisch und Französisch erstellt wird.

**So erstellen Sie eine MUI-Datei für Englisch und Französisch**

1.  Erstellen Sie eine Meldungs Textdatei, die die französischen Nachrichten Zeichenfolgen erstellt. Ausführliche Informationen zum Erstellen einer Meldungs Textdatei finden Sie unter [Message Text Files](/windows/desktop/EventLog/message-text-files). Die Nachrichten-IDs, die Sie in der Meldungs Textdatei angeben, müssen mit den Ressourcen Bezeichner übereinstimmen, die der Nachrichten Compiler für dieselben Zeichen folgen im Manifest generiert hat. Um die Ressourcen Bezeichner zu ermitteln, die für die Zeichen folgen im Manifest verwendet werden, sehen Sie sich die h-Datei an, die der Nachrichten Compiler beim Kompilieren des Manifests generiert hat.
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  Führen Sie die folgenden Befehle aus, um die Ressourcen-DLL zu erstellen, die ihre lokalisierten Zeichen folgen enthält Die Datei Messages.MC ist die Nachrichten Textdatei, die Sie in Schritt 1 erstellt haben.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Erstellen Sie in dem Ordner, der Ihren Anbieter enthält, einen Unterordner für jedes Gebiets Schema, das Sie unterstützen. Der Name des unter Ordners muss der Sprachen Name für dieses Gebiets Schema sein. Verwenden Sie z. b. für 0x0409 en-US als Ordnernamen.
4.  Erstellen Sie eine rcconfig-Datei, die dem Muirct.exe Tool mitteilt, dass Sie die Nachrichten Zeichen folgen Ressourcen aus der ausführbaren Datei und den Ressourcen-DLLs aufteilen möchten. Im folgenden finden Sie ein Beispiel für eine rcconfig-Beispieldatei.
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  Führen Sie die folgenden Muirct.exe Befehle aus, um die englischen Zeichen folgen aus der ausführbaren Datei des Anbieters aufzuteilen.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Führen Sie die folgenden Muirct.exe Befehle aus, um die französischen Zeichen folgen aus der Ressourcen-DLL aufzuteilen. Entfernen Sie die sprachneutrale Datei (fr-FR \\messages.dll), nachdem die MUI-Datei erstellt wurde.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Benennen Sie provider.exe. ln in provider.exe um.