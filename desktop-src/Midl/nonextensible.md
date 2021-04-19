---
title: nonextensible-Attribut
description: Das \ nonextensible \-Attribut gibt an, dass die IDispatch-Implementierung nur die Eigenschaften und Methoden enthält, die in der Schnittstellen Beschreibung aufgeführt sind, und kann zur Laufzeit nicht mit zusätzlichen Elementen erweitert werden.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- nicht erweiterbares Attribut, Mittel l
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339057"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="c93a0-104">nonextensible-Attribut</span><span class="sxs-lookup"><span data-stu-id="c93a0-104">nonextensible attribute</span></span>

<span data-ttu-id="c93a0-105">Das **\[ nonextensible \]** -Attribut gibt an, dass die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Implementierung nur die Eigenschaften und Methoden enthält, die in der Schnittstellen Beschreibung aufgeführt sind, und kann zur Laufzeit nicht mit zusätzlichen Elementen erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="c93a0-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="c93a0-106">(In der Standardeinstellung geht es bei der Automatisierung davon aus, dass Schnittstellen Elemente zur Laufzeit hinzufügen können, d. h., Sie sind erweiterbar.)</span><span class="sxs-lookup"><span data-stu-id="c93a0-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="c93a0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c93a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93a0-108">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="c93a0-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="c93a0-109">Gibt eine universell eindeutige Identifikationsnummer für die [**Schnittstelle**](interface.md)an.</span><span class="sxs-lookup"><span data-stu-id="c93a0-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93a0-110">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="c93a0-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c93a0-111">Gibt eine Liste von 0 (null) oder mehr Attributen der Mittelwert Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="c93a0-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c93a0-112">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="c93a0-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c93a0-113">Gibt den Namen der [**Schnittstelle**](interface.md) oder der " [**dispinterface**](dispinterface.md)" an.</span><span class="sxs-lookup"><span data-stu-id="c93a0-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93a0-114">*Schnittstellen Definition*</span><span class="sxs-lookup"><span data-stu-id="c93a0-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="c93a0-115">Gibt IDL-Anweisungen an, die die Definition der- [**Schnittstelle**](interface.md) oder der [**dispinterface**](dispinterface.md)bilden.</span><span class="sxs-lookup"><span data-stu-id="c93a0-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c93a0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c93a0-116">Remarks</span></span>

<span data-ttu-id="c93a0-117">Sie können das **\[ nonextensible \]** -Attribut entweder auf eine Schnittstelle oder eine dispinterface anwenden.</span><span class="sxs-lookup"><span data-stu-id="c93a0-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="c93a0-118">Eine Schnittstelle muss jedoch auch über die **\[** [**Dual**](dual.md) **\]** -und **\[** [**oleautomation**](oleautomation.md) - **\]** Attribute verfügen.</span><span class="sxs-lookup"><span data-stu-id="c93a0-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="c93a0-119">Flags</span><span class="sxs-lookup"><span data-stu-id="c93a0-119">Flags</span></span>

<span data-ttu-id="c93a0-120">TYPEFLAG- \_ nicht erweiterbar</span><span class="sxs-lookup"><span data-stu-id="c93a0-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="c93a0-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c93a0-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c93a0-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c93a0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93a0-123">Inhalt einer Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c93a0-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="c93a0-124">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="c93a0-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="c93a0-125">**Ales**</span><span class="sxs-lookup"><span data-stu-id="c93a0-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="c93a0-126">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="c93a0-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c93a0-127">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="c93a0-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c93a0-128">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="c93a0-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c93a0-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="c93a0-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="c93a0-130">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c93a0-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 