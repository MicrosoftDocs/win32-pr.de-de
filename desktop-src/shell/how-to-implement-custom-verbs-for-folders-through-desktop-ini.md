---
description: In Windows 7 und höher können Sie mit Desktop.ini Verben zu einem Ordner hinzufügen. Weitere Informationen zu Desktop.ini Dateien finden Sie unter Anpassen von Ordnern mit Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: So implementieren Sie benutzerdefinierte Verben für Ordner über Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979545"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="65db0-104">So implementieren Sie benutzerdefinierte Verben für Ordner über Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="65db0-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="65db0-105">In Windows 7 und höher können Sie mit Desktop.ini Verben zu einem Ordner hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65db0-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="65db0-106">Weitere Informationen zu Desktop.ini Dateien finden Sie unter [Anpassen von Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="65db0-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="65db0-107">Desktop.ini Dateien sollten immer als ausgeblendet **markiert werden**  +   , damit Sie Benutzern nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="65db0-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="65db0-108">Um benutzerdefinierte Verben für Ordner über eine Desktop.ini Datei hinzuzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="65db0-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="65db0-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="65db0-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="65db0-110">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="65db0-110">Step 1:</span></span>

<span data-ttu-id="65db0-111">Erstellen **Sie** einen Ordner, der als schreibgeschützt oder als **System** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="65db0-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="65db0-112">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="65db0-112">Step 2:</span></span>

<span data-ttu-id="65db0-113">Erstellen Sie eine Desktop.ini-Datei, die eine enthält \[ . Shellclassinfo \] directoryclass = Ordner ProgID.</span><span class="sxs-lookup"><span data-stu-id="65db0-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="65db0-114">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="65db0-114">Step 3:</span></span>

<span data-ttu-id="65db0-115">Erstellen Sie in der Registrierung **HKEY \_ - \_ Klassen** \\ **Stamm Ordner ProgID** mit dem Wert "canusefordirectory".</span><span class="sxs-lookup"><span data-stu-id="65db0-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="65db0-116">Der Wert von "canusefordirectory" vermeidet den Missbrauch von ProgIDs, die nicht an der Implementierung benutzerdefinierter Verben für Ordner durch Desktop.ini beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="65db0-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="65db0-117">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="65db0-117">Step 4:</span></span>

<span data-ttu-id="65db0-118">Fügen Sie unter dem **Ordner** ProgID Unterschlüssel Verben hinzu, z. b.:</span><span class="sxs-lookup"><span data-stu-id="65db0-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="65db0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65db0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65db0-120">Diese Verben können die Standard Verben sein. in diesem Fall wird das Verb durch Doppelklicken auf den Ordner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="65db0-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



