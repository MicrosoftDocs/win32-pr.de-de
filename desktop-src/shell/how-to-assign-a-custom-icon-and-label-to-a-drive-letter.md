---
description: Geben Sie ein benutzerdefiniertes Symbol und eine Bezeichnung für ein Laufwerk an.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Zuweisen eines benutzerdefinierten Symbols und einer Bezeichnung zu einem Laufwerk Buchstaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979632"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="978b3-103">Zuweisen eines benutzerdefinierten Symbols und einer Bezeichnung zu einem Laufwerk Buchstaben</span><span class="sxs-lookup"><span data-stu-id="978b3-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="978b3-104">Geben Sie ein benutzerdefiniertes Symbol und eine Bezeichnung für ein Laufwerk an.</span><span class="sxs-lookup"><span data-stu-id="978b3-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="978b3-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="978b3-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="978b3-106">Schritt 1: Ersetzen des Standard-Laufwerk Symbols durch ein benutzerdefiniertes Symbol in Windows 2000</span><span class="sxs-lookup"><span data-stu-id="978b3-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="978b3-107">Um das Standard Laufwerk Symbol durch ein benutzerdefiniertes Symbol in Windows 2000 zu ersetzen, fügen Sie dem folgenden Schlüssel einen Unterschlüssel mit dem Namen für den Laufwerk Buchstaben hinzu.</span><span class="sxs-lookup"><span data-stu-id="978b3-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="978b3-108">Im folgenden Beispiel wird ein benutzerdefiniertes Symbol und eine Bezeichnung für das Laufwerk E: angegeben.</span><span class="sxs-lookup"><span data-stu-id="978b3-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="978b3-109">Das Symbol befindet sich in der Datei "C: \\ mydir \\MyDrive.exe" mit einem NULL basierten Index von drei.</span><span class="sxs-lookup"><span data-stu-id="978b3-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="978b3-110">Für Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="978b3-110">For Windows 2000:</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="978b3-111">Schritt 2: Ersetzen des Standard-Laufwerk Symbols durch ein benutzerdefiniertes Symbol in allen anderen Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="978b3-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="978b3-112">Um das Standard Laufwerk Symbol durch ein benutzerdefiniertes Symbol in allen Windows-Versionen außer Windows 2000 zu ersetzen, fügen Sie dem folgenden Schlüssel einen Unterschlüssel mit dem Namen für den Laufwerk Buchstaben hinzu.</span><span class="sxs-lookup"><span data-stu-id="978b3-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="978b3-113">Im folgenden Beispiel wird ein benutzerdefiniertes Symbol und eine Bezeichnung für das Laufwerk E: angegeben.</span><span class="sxs-lookup"><span data-stu-id="978b3-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="978b3-114">Das Symbol befindet sich in der Datei "C: \\ mydir \\MyDrive.exe" mit einem NULL basierten Index von drei.</span><span class="sxs-lookup"><span data-stu-id="978b3-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="978b3-115">Für alle anderen Versionen von Windows:</span><span class="sxs-lookup"><span data-stu-id="978b3-115">For all other versions of Windows:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="978b3-116">Schritt 3: Aufrufen des shupdateimage-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="978b3-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="978b3-117">Wenn Sie in allen Versionen von Windows einen Dateityp oder ein Laufwerk Symbol ändern, müssen Sie auch shupdateimage aufrufen, um die Shell zu benachrichtigen, dass derzeit angezeigte Symbole aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="978b3-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="978b3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="978b3-118">Remarks</span></span>

<span data-ttu-id="978b3-119">Auf den Laufwerk Buchstaben darf kein Doppelpunkt (:).</span><span class="sxs-lookup"><span data-stu-id="978b3-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="978b3-120">Fügen Sie dem Unterschlüssel Laufwerksbuchstabe einen **DefaultIcon** -Unterschlüssel hinzu, und legen Sie dessen Standardwert auf eine Zeichenfolge fest, die den Speicherort des Symbols enthält.</span><span class="sxs-lookup"><span data-stu-id="978b3-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="978b3-121">Der erste Teil der Zeichenfolge enthält den voll qualifizierten Pfad der Symbol Datei.</span><span class="sxs-lookup"><span data-stu-id="978b3-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="978b3-122">Wenn in der Datei mehr als ein Symbol vorhanden ist, folgt der Pfad ein Komma und dann der null basierte Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="978b3-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



