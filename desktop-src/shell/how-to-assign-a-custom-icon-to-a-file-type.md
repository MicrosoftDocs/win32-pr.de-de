---
description: Ein benutzerdefiniertes Symbol muss einem Dateityp zugewiesen werden, um dem Benutzer dieses Dateityps oder der Anwendung, der der Dateityp zugeordnet ist, einen visuellen Hinweis zu geben.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Zuweisen eines benutzerdefinierten Symbols zu einem Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979617"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="920b1-103">Zuweisen eines benutzerdefinierten Symbols zu einem Dateityp</span><span class="sxs-lookup"><span data-stu-id="920b1-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="920b1-104">Wenn einem Dateityp kein benutzerdefiniertes Standard Symbol zugewiesen ist, zeigen der Desktop und Windows-Explorer alle Dateien dieses Typs mit einem generischen Standard Symbol an.</span><span class="sxs-lookup"><span data-stu-id="920b1-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="920b1-105">Der folgende Screenshot zeigt z. b. das Standard Symbol, das mit der Datei MyDocs4. MYP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="920b1-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![Screenshot des Standard Symbols](images/icon.png)

<span data-ttu-id="920b1-107">Obwohl es sich bei allen in diesem Screenshot angezeigten Dateien um einfache Textdateien handelt, zeigt nur MyDocs4. MYP das Windows-Standard Symbol an.</span><span class="sxs-lookup"><span data-stu-id="920b1-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="920b1-108">Dies liegt daran, dass die Erweiterung ". txt" ein registrierter Dateityp mit einem benutzerdefinierten Standard Symbol ist.</span><span class="sxs-lookup"><span data-stu-id="920b1-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="920b1-109">Der folgende Screenshot zeigt ein benutzerdefiniertes Symbol, das dem Dateityp MYP zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="920b1-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![Screenshot des benutzerdefinierten Symbols für MYP-Dateien](images/context4.png)

> [!Note]  
> <span data-ttu-id="920b1-111">Symbole können auch anwendungsspezifisch zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="920b1-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="920b1-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="920b1-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="920b1-113">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="920b1-113">Step 1:</span></span>

<span data-ttu-id="920b1-114">Erstellen Sie einen Unterschlüssel mit dem Namen **DefaultIcon** an einem der beiden folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="920b1-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="920b1-115">Für eine Dateityp Zuweisung, **HKEY- \_ Klassen \_ root** \\ *. Extension*</span><span class="sxs-lookup"><span data-stu-id="920b1-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="920b1-116">Für eine Anwendungs Zuweisung, **HKEY \_ - \_ Klassen** \\ *Stamm-ProgID*</span><span class="sxs-lookup"><span data-stu-id="920b1-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="920b1-117">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="920b1-117">Step 2:</span></span>

<span data-ttu-id="920b1-118">Weisen Sie den Unterschlüssel **DefaultIcon** einem Standardwert des Typs **reg \_ SZ** zu, der den voll qualifizierten Pfad für die Datei angibt, in der das Symbol enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="920b1-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="920b1-119">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="920b1-119">Step 3:</span></span>

<span data-ttu-id="920b1-120">Rufen Sie die [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) -Funktion auf, um die Shell zu benachrichtigen, ihren Symbol Cache zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="920b1-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="920b1-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="920b1-121">Remarks</span></span>

<span data-ttu-id="920b1-122">Das folgende Beispiel zeigt eine detaillierte Ansicht der Registrierungseinträge, die für eine Dateityp-Symbol Zuweisung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="920b1-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="920b1-123">Die Dateinamenerweiterung ist einer Anwendung zugeordnet, aber die Symbol Zuweisung erfolgt in der Dateinamenerweiterung selbst, sodass die zugehörige Anwendung das Standard Symbol nicht vorschreibt.</span><span class="sxs-lookup"><span data-stu-id="920b1-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="920b1-124">Das folgende Beispiel zeigt eine detaillierte Ansicht der Registrierungseinträge, die für eine Anwendungssymbol Zuweisung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="920b1-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="920b1-125">Die Dateinamenerweiterung MYP ist zuerst der Anwendung MyProgram. 1 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="920b1-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="920b1-126">Dem Unterschlüssel MyProgram. 1 ProgID wird dann das benutzerdefinierte Standard Symbol zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="920b1-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="920b1-127">Jede Datei, die ein Symbol enthält, ist akzeptabel, einschließlich ICO-, exe-und dll-Dateien.</span><span class="sxs-lookup"><span data-stu-id="920b1-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="920b1-128">Wenn in der Datei mehr als ein Symbol vorhanden ist, muss auf den Pfad ein Komma und dann auf den Index des Symbols folgen.</span><span class="sxs-lookup"><span data-stu-id="920b1-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="920b1-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="920b1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920b1-130">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="920b1-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



