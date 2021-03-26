---
description: Definieren von Dateityp Attributen in der Registrierung.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Definieren von Dateityp Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864931"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="4b209-103">Definieren von Dateityp Attributen</span><span class="sxs-lookup"><span data-stu-id="4b209-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="4b209-104">Durch das Zuweisen von Dateityp Attributen zu einer zugeordneten ProgID können Sie einige Aspekte des Verhaltens des Dateityps steuern.</span><span class="sxs-lookup"><span data-stu-id="4b209-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="4b209-105">Vor Windows Vista konnten diese Attribute Ihnen ermöglichen, den Umfang zu beschränken, in dem der Benutzer die Eigenschaften Registerkarte **Ordneroptionen** verwenden könnte, um verschiedene Aspekte des Dateityps zu ändern, z. b. das Symbol oder die Verben.</span><span class="sxs-lookup"><span data-stu-id="4b209-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="4b209-106">Dateityp Attribute sind binäre Flags, die als **reg \_ DWORD** -oder **reg- \_ Binär** Werte im zugeordneten ProgID-Unterschlüssel des Dateityps angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b209-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="4b209-107">Um Attribute für einen Dateityp zuzuweisen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4b209-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="4b209-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="4b209-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="4b209-109">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="4b209-109">Step 1:</span></span>

<span data-ttu-id="4b209-110">Fügen Sie dem zugeordneten ProgID-Unterschlüssel des Dateityps einen EditFlags-Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b209-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="4b209-111">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="4b209-111">Step 2:</span></span>

<span data-ttu-id="4b209-112">Legen Sie den Eintrag auf den entsprechenden Attribut Wert fest.</span><span class="sxs-lookup"><span data-stu-id="4b209-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="4b209-113">Im folgenden Beispiel werden die \_ für den MYP-Dateityp festgelegten Attribute "FTA NoRemove (0x00000010)" und "FTA \_ nonewverb (0x00000020)" gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b209-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="4b209-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b209-114">Remarks</span></span>

<span data-ttu-id="4b209-115">Die Flags können mit einem logischen OR kombiniert werden, um den Wert eines einzelnen Attributs zu bilden.</span><span class="sxs-lookup"><span data-stu-id="4b209-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="4b209-116">Eine Liste der möglichen Dateityp Attribute und ihrer hexadezimalen Werte sowie weitere Informationen zum programmgesteuerten abrufen und Festlegen dieser Werte finden Sie unter [**filetypeattributeflags**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span><span class="sxs-lookup"><span data-stu-id="4b209-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



