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
# <a name="localizing-message-strings"></a><span data-ttu-id="208c7-103">Lokalisieren von Meldungs Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="208c7-103">Localizing Message Strings</span></span>

<span data-ttu-id="208c7-104">Jede Nachrichten Zeichenfolge, die Sie im Manifest angeben, muss im **Lokalisierungs** Abschnitt des Manifests auf eine Zeichenfolge verweisen.</span><span class="sxs-lookup"><span data-stu-id="208c7-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="208c7-105">Der Abschnitt Lokalisierung enthält einen Zeichen folgen Tabellen Abschnitt für jedes Gebiets Schema, das Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="208c7-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="208c7-106">Im folgenden Beispiel wird gezeigt, wie eine Zeichen folgen Tabelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="208c7-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="208c7-107">Sie müssen die Attribute **ID** und **value** der Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="208c7-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="208c7-108">Sie verwenden den Wert des **ID** -Attributs, um auf die Zeichenfolge im Manifest zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="208c7-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="208c7-109">Das **value** -Attribut enthält die lokalisierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="208c7-109">The **value** attribute contains the localized string.</span></span>


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


<span data-ttu-id="208c7-110">Anstatt dem Manifest lokalisierte Zeichen folgen hinzuzufügen, sollten Sie eine MUI-Datei (mehrsprachige Benutzeroberfläche) für jede Sprache erstellen, die Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="208c7-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="208c7-111">Verwenden Sie eine Meldungs Textdatei, um die lokalisierten Zeichen folgen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="208c7-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="208c7-112">Im folgenden Verfahren wird beschrieben, wie eine MUI-Datei für Englisch und Französisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="208c7-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="208c7-113">**So erstellen Sie eine MUI-Datei für Englisch und Französisch**</span><span class="sxs-lookup"><span data-stu-id="208c7-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="208c7-114">Erstellen Sie eine Meldungs Textdatei, die die französischen Nachrichten Zeichenfolgen erstellt.</span><span class="sxs-lookup"><span data-stu-id="208c7-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="208c7-115">Ausführliche Informationen zum Erstellen einer Meldungs Textdatei finden Sie unter [Message Text Files](/windows/desktop/EventLog/message-text-files).</span><span class="sxs-lookup"><span data-stu-id="208c7-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="208c7-116">Die Nachrichten-IDs, die Sie in der Meldungs Textdatei angeben, müssen mit den Ressourcen Bezeichner übereinstimmen, die der Nachrichten Compiler für dieselben Zeichen folgen im Manifest generiert hat.</span><span class="sxs-lookup"><span data-stu-id="208c7-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="208c7-117">Um die Ressourcen Bezeichner zu ermitteln, die für die Zeichen folgen im Manifest verwendet werden, sehen Sie sich die h-Datei an, die der Nachrichten Compiler beim Kompilieren des Manifests generiert hat.</span><span class="sxs-lookup"><span data-stu-id="208c7-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
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


2.  <span data-ttu-id="208c7-118">Führen Sie die folgenden Befehle aus, um die Ressourcen-DLL zu erstellen, die ihre lokalisierten Zeichen folgen enthält</span><span class="sxs-lookup"><span data-stu-id="208c7-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="208c7-119">Die Datei Messages.MC ist die Nachrichten Textdatei, die Sie in Schritt 1 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="208c7-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="208c7-120">Erstellen Sie in dem Ordner, der Ihren Anbieter enthält, einen Unterordner für jedes Gebiets Schema, das Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="208c7-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="208c7-121">Der Name des unter Ordners muss der Sprachen Name für dieses Gebiets Schema sein.</span><span class="sxs-lookup"><span data-stu-id="208c7-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="208c7-122">Verwenden Sie z. b. für 0x0409 en-US als Ordnernamen.</span><span class="sxs-lookup"><span data-stu-id="208c7-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="208c7-123">Erstellen Sie eine rcconfig-Datei, die dem Muirct.exe Tool mitteilt, dass Sie die Nachrichten Zeichen folgen Ressourcen aus der ausführbaren Datei und den Ressourcen-DLLs aufteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="208c7-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="208c7-124">Im folgenden finden Sie ein Beispiel für eine rcconfig-Beispieldatei.</span><span class="sxs-lookup"><span data-stu-id="208c7-124">The following is an example .rcconfig file.</span></span>
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
  

5.  <span data-ttu-id="208c7-125">Führen Sie die folgenden Muirct.exe Befehle aus, um die englischen Zeichen folgen aus der ausführbaren Datei des Anbieters aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="208c7-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="208c7-126">Führen Sie die folgenden Muirct.exe Befehle aus, um die französischen Zeichen folgen aus der Ressourcen-DLL aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="208c7-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="208c7-127">Entfernen Sie die sprachneutrale Datei (fr-FR \\messages.dll), nachdem die MUI-Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="208c7-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="208c7-128">Benennen Sie provider.exe. ln in provider.exe um.</span><span class="sxs-lookup"><span data-stu-id="208c7-128">Rename provider.exe.ln to provider.exe.</span></span>