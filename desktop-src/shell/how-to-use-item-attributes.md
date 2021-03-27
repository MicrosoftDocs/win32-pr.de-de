---
description: Die sfgao-Flagwerte der shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Verwenden von Element Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864912"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="9d982-103">Verwenden von Element Attributen</span><span class="sxs-lookup"><span data-stu-id="9d982-103">How to Use Item Attributes</span></span>

<span data-ttu-id="9d982-104">Die [**sfgao**](sfgao.md) -Flagwerte der shellattribute für ein Element können getestet werden, um zu bestimmen, ob das Verb aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d982-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="9d982-105">Um dieses Attribut zu verwenden, fügen Sie die folgenden **reg \_ DWORD** -Werte unter dem Verb hinzu:</span><span class="sxs-lookup"><span data-stu-id="9d982-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="9d982-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="9d982-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="9d982-107">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="9d982-107">Step 1:</span></span>

<span data-ttu-id="9d982-108">Der attributemask-Wert gibt den [**sfgao**](sfgao.md) -Wert der Bitwerte der Maske an, die getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d982-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="9d982-109">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="9d982-109">Step 2:</span></span>

<span data-ttu-id="9d982-110">Der AttributeValue-Wert gibt den [**sfgao**](sfgao.md) -Wert der zu testenden Bits an.</span><span class="sxs-lookup"><span data-stu-id="9d982-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="9d982-111">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="9d982-111">Step 3:</span></span>

<span data-ttu-id="9d982-112">Das impliedselectionmodel gibt 0 (null) für Element Verben oder einen Wert ungleich 0 (null) für Verben im Hintergrund Kontextmenü an.</span><span class="sxs-lookup"><span data-stu-id="9d982-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d982-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d982-113">Remarks</span></span>

<span data-ttu-id="9d982-114">Im folgenden Beispiel Registrierungs Eintrag wird attributemask auf [**sfgao \_**](sfgao.md) schreibgeschützt (0x40000) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d982-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



