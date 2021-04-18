---
title: Load-Methode
description: Load-Methode
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337425"
---
# <a name="load-method"></a><span data-ttu-id="1ff81-103">Load-Methode</span><span class="sxs-lookup"><span data-stu-id="1ff81-103">Load Method</span></span>

<span data-ttu-id="1ff81-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1ff81-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1ff81-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ff81-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1ff81-106">Lädt ein Zeichen in die [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1ff81-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="1ff81-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1ff81-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1ff81-108">\*Agent ***. Zeichen. Load "*** Merkmal-ID \* *",* \*  *Anbieter*</span><span class="sxs-lookup"><span data-stu-id="1ff81-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="1ff81-109">Teil</span><span class="sxs-lookup"><span data-stu-id="1ff81-109">Part</span></span>          | <span data-ttu-id="1ff81-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ff81-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff81-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="1ff81-111">*CharacterID*</span></span> | <span data-ttu-id="1ff81-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ff81-112">Required.</span></span> <span data-ttu-id="1ff81-113">Ein Zeichen folgen Wert, mit dem auf die zu ladenden Zeichendaten verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1ff81-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="1ff81-114">*Anbieter*</span><span class="sxs-lookup"><span data-stu-id="1ff81-114">*Provider*</span></span>    | <span data-ttu-id="1ff81-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ff81-115">Required.</span></span> <span data-ttu-id="1ff81-116">Ein Variant-Datentyp, bei dem es sich um einen der folgenden Typen handeln muss: **filespec** der lokale Datei Speicherort der Definitionsdatei des angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="1ff81-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="1ff81-117">**URL** Die http-Adresse für die Definitionsdatei des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="1ff81-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ff81-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ff81-118">Remarks</span></span>

<span data-ttu-id="1ff81-119">Sie können Zeichen aus dem Unterverzeichnis des Agents laden, indem Sie einen relativen Pfad angeben (einer, der keinen Doppelpunkt oder vorangestellenden Schrägstrich enthält).</span><span class="sxs-lookup"><span data-stu-id="1ff81-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="1ff81-120">Dadurch wird der Pfad mit dem Zeichen Verzeichnis des Agents (befindet sich im lokalisierten Windows \\ MSAgent-Verzeichnis) als Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="1ff81-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="1ff81-121">Wenn Sie z. b. Folgendes angeben, wird Genie. ACS aus dem chars-Verzeichnis des Agents geladen:</span><span class="sxs-lookup"><span data-stu-id="1ff81-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="1ff81-122">Sie können auch Ihr eigenes Verzeichnis im chars-Verzeichnis des Agents angeben.</span><span class="sxs-lookup"><span data-stu-id="1ff81-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="1ff81-123">Sie können das Zeichen, das momentan als Standard Zeichen des aktuellen Benutzers festgelegt ist, laden, indem Sie keinen Pfad als zweiten Parameter der **Load** -Methode einschließen.</span><span class="sxs-lookup"><span data-stu-id="1ff81-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="1ff81-124">Es ist nicht möglich, dasselbe Zeichen (ein Zeichen mit derselben GUID) mehrmals aus einer einzelnen Instanz des Steuer Elements zu laden.</span><span class="sxs-lookup"><span data-stu-id="1ff81-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="1ff81-125">Ebenso können Sie das Standard Zeichen und andere Zeichen nicht gleichzeitig von einer einzelnen Instanz des Steuer Elements laden, da das Standard Zeichen mit dem anderen Zeichen identisch sein könnte.</span><span class="sxs-lookup"><span data-stu-id="1ff81-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="1ff81-126">Wenn Sie versuchen, dies zu tun, löst der Server einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="1ff81-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="1ff81-127">Sie können jedoch eine weitere Instanz des agentsteuerelements erstellen und dasselbe Zeichen laden.</span><span class="sxs-lookup"><span data-stu-id="1ff81-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="1ff81-128">Der Microsoft-Agent Datenanbieter unterstützt das Laden von Zeichendaten, die entweder als einzelne strukturierte Datei () gespeichert werden. ACS) mit Zeichendaten und Animationsdaten oder als separate Zeichendaten (. ACF) und Animation (. ACA-Dateien.</span><span class="sxs-lookup"><span data-stu-id="1ff81-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="1ff81-129">Verwenden Sie die strukturierte Struktur. Die ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Datenträger oder Netzwerk gespeichert wird und auf das mithilfe eines herkömmlichen Datei Protokolls (z. b. UNC-Pfadnamen) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="1ff81-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="1ff81-130">Verwenden Sie die separate. ACF und. ACA-Dateien, wenn Sie die Animationsdateien einzeln von einer Remote Site laden möchten, auf die über das HTTP-Protokoll zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="1ff81-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="1ff81-131">Damit. ACS-Dateien, die die **Load** -Methode verwenden, bieten Zugriff auf die Animationen eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="1ff81-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="1ff81-132">Damit. ACF-Dateien verwenden Sie auch die [**Get**](get-method.md) -Methode, um Animationsdaten zu laden.</span><span class="sxs-lookup"><span data-stu-id="1ff81-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="1ff81-133">Die **Load** -Methode unterstützt nicht das herunterladen. ACS-Dateien von einer HTTP-Site.</span><span class="sxs-lookup"><span data-stu-id="1ff81-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="1ff81-134">Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1ff81-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="1ff81-135">Verwenden Sie zuerst die [**Show**](show-method.md) -Methode, um das Zeichen sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="1ff81-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="1ff81-136">Wenn Sie die **Load** -Methode verwenden, um eine auf dem lokalen Computer gespeicherte Zeichen Datei zu laden, schlägt der-Befehl fehl. Da die Datei z. b. nicht gefunden wird, löst der-Agent einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="1ff81-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="1ff81-137">Mithilfe der-Unterstützung in der Programmiersprache können Sie eine Fehler Behandlungs Routine bereitstellen, um den Fehler zu erfassen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ff81-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



<span data-ttu-id="1ff81-138">Sie können den Fehler auch behandeln, indem Sie [**raiserequesterrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) auf **false** festlegen, ein-Objekt deklarieren und ihm die **Lade** Anforderung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1ff81-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="1ff81-139">Befolgen Sie dann den **Lade** Vorgang mit einer-Anweisung, die den Status des [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts überprüft.</span><span class="sxs-lookup"><span data-stu-id="1ff81-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



<span data-ttu-id="1ff81-140">Wenn Sie ein nicht lokales Zeichen laden. Beispielsweise können Sie mithilfe des HTTP-Protokolls auch überprüfen, ob ein **Lade** Fehler vorliegt, indem Sie der **Load** -Methode ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1ff81-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="1ff81-141">Da diese Methode zum Laden eines Zeichens jedoch asynchron verarbeitet wird, überprüfen Sie seinen Status im [**requestcomplete**](requestcomplete-event.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1ff81-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="1ff81-142">Dieses Verfahren funktioniert nicht, wenn ein Zeichen mithilfe des UNC-Protokolls geladen wird, da die **Load** -Methode synchron verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="1ff81-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 

