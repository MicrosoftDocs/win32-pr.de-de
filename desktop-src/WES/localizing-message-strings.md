---
title: Lokalisieren von Meldungszeichenfolgen
description: Jede Meldungszeichenfolge, die Sie im Manifest angeben, muss auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests verweisen.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55b94ea8e8a40de1401cf3aba97488d5531a77b441361e38f1ff98219940afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587898"
---
# <a name="localizing-message-strings"></a>Lokalisieren von Meldungszeichenfolgen

Jede Meldungszeichenfolge, die Sie im Manifest  angeben, muss auf eine Zeichenfolge im Lokalisierungsabschnitt des Manifests verweisen. Der Lokalisierungsabschnitt enthält einen Zeichenfolgentabellenabschnitt für jedes von Ihnen unterstützte Locale.

Das folgende Beispiel zeigt, wie eine Zeichenfolgentabelle definiert wird. Sie müssen die Id- und **Wertattribute** **der** Zeichenfolge angeben. Sie verwenden den Wert des **ID-Attributs,** um auf die Zeichenfolge in Ihrem Manifest zu verweisen. Das **Value-Attribut** enthält die lokalisierte Zeichenfolge.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
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


Anstatt lokalisierte Zeichenfolgen zum Manifest hinzufügen zu müssen, sollten Sie eine mehrsprachige Benutzeroberflächendatei (MULTILINGUAL) für jede Sprache erstellen, die Sie unterstützen. Verwenden Sie eine Meldungstextdatei, um ihre lokalisierten Zeichenfolgen anzugeben.

Im folgenden Verfahren wird beschrieben, wie Eine -DATEI für Englisch und Französisch erstellt wird.

**So erstellen Sie eine ANWEISUNG-Datei für Englisch und Französisch**

1.  Erstellen Sie eine Meldungstextdatei, die die französischen Nachrichtenzeichenfolgen erstellt. Weitere Informationen zum Erstellen einer Nachrichtentextdatei finden Sie unter [Nachrichtentextdateien](/windows/desktop/EventLog/message-text-files). Die Nachrichtenbezeichner, die Sie in der Meldungstextdatei angeben, müssen mit den Ressourcenbezeichnern übereinstimmen, die der Nachrichtencompiler für die gleichen Zeichenfolgen im Manifest generiert hat. Informationen zum Bestimmen der Ressourcenbezeichner, die für die Zeichenfolgen im Manifest verwendet werden, finden Sie in der H-Datei, die der Nachrichtencompiler beim Kompilieren des Manifests generiert hat.
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


2.  Führen Sie die folgenden Befehle aus, um die Ressourcen-DLL zu erstellen, die ihre lokalisierten Zeichenfolgen enthält. Die messages.mc ist die Meldungstextdatei, die Sie in Schritt 1 erstellt haben.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Erstellen Sie in dem Ordner, der Ihren Anbieter enthält, einen Unterordner für jedes von Ihnen unterstützte Locale. Der Name des Unterordners muss der Sprachname für dieses Locale sein. Verwenden Sie für 0x0409 z. B. en-US als Ordnernamen.
4.  Erstellen Sie eine RCCONFIG-Datei, die dem Muirct.exe angibt, dass Sie die Nachrichtenzeichenfolgenressourcen von der ausführbaren Datei und den Ressourcen-DLLs aufteilen möchten. Im Folgenden finden Sie eine RCCONFIG-Beispieldatei.
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
  

5.  Führen Sie die folgenden Muirct.exe aus, um die englischen Zeichenfolgen aus der ausführbaren Datei des Anbieters zu teilen.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Führen Sie die folgenden Muirct.exe aus, um die französischen Zeichenfolgen von der Ressourcen-DLL zu trennen. Entfernen Sie die sprachneutrale Datei (fr-FR \\messages.dll), nachdem die DATEI MIT-Anweisung erstellt wurde.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Benennen provider.exe.ln in provider.exe.
