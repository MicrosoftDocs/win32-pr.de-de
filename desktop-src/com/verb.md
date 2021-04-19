---
title: Verb
description: Gibt die Verben an, die für eine Anwendung registriert werden sollen.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Verb Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339101"
---
# <a name="verb"></a><span data-ttu-id="b562a-104">Verb</span><span class="sxs-lookup"><span data-stu-id="b562a-104">Verb</span></span>

<span data-ttu-id="b562a-105">Gibt die Verben an, die für eine Anwendung registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b562a-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b562a-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="b562a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="b562a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b562a-107">Remarks</span></span>

<span data-ttu-id="b562a-108">Jedes Verb ist ein **reg \_ SZ** -Wert im Format "*Name*, *Menü \_* Kennzeichen, *Verb \_ Flag*".</span><span class="sxs-lookup"><span data-stu-id="b562a-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="b562a-109">Verben müssen nacheinander nummeriert werden.</span><span class="sxs-lookup"><span data-stu-id="b562a-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="b562a-110">Der *Name* beschreibt, wie das Verb durch einen [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) -Funktions aufrufangefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b562a-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="b562a-111">Beispiel: "&Play".</span><span class="sxs-lookup"><span data-stu-id="b562a-111">For example, "&Play".</span></span>

<span data-ttu-id="b562a-112">Der Wert für das *\_ menüflag* gibt an, wie das Verb im Menü angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b562a-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="b562a-113">Alle Flags, die von [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) unterstützt werden, werden unterstützt, mit Ausnahme von MF- \_ Bitmap, MF \_ -Besitzer zeichnen und MF- \_ Popup.</span><span class="sxs-lookup"><span data-stu-id="b562a-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="b562a-114">Der *Verb \_ Flagwert* beschreibt die Attribute der Verben.</span><span class="sxs-lookup"><span data-stu-id="b562a-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="b562a-115">Verwenden Sie einen der Werte aus [**oleverbatbinb**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)oder 0.</span><span class="sxs-lookup"><span data-stu-id="b562a-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="b562a-116">Weitere Informationen finden Sie unter [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)und [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span><span class="sxs-lookup"><span data-stu-id="b562a-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b562a-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b562a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b562a-118">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="b562a-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="b562a-119">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="b562a-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="b562a-120">**Oleverbatbinb**</span><span class="sxs-lookup"><span data-stu-id="b562a-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 