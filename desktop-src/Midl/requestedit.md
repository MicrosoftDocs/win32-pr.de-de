---
title: requestedit-Attribut
description: Das Attribut \ requestedit \ gibt an, dass die Eigenschaft die OnRequestEdit-Benachrichtigung unterstützt.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit-Attribut-Mittel l
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338254"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="3710a-104">requestedit-Attribut</span><span class="sxs-lookup"><span data-stu-id="3710a-104">requestedit attribute</span></span>

<span data-ttu-id="3710a-105">Das **\[ requestedit \]** -Attribut gibt an, dass die Eigenschaft die **OnRequestEdit** -Benachrichtigung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3710a-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="3710a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3710a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3710a-107">*optionale Attribute*</span><span class="sxs-lookup"><span data-stu-id="3710a-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="3710a-108">NULL oder mehr mittlere Attribute.</span><span class="sxs-lookup"><span data-stu-id="3710a-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3710a-109">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="3710a-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="3710a-110">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="3710a-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="3710a-111">*function-name*</span><span class="sxs-lookup"><span data-stu-id="3710a-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3710a-112">Gibt den Namen der Funktion in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="3710a-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="3710a-113">*params*</span><span class="sxs-lookup"><span data-stu-id="3710a-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3710a-114">NULL oder mehr Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="3710a-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3710a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3710a-115">Remarks</span></span>

<span data-ttu-id="3710a-116">Die Unterstützung der **OnRequestEdit** -Benachrichtigung bedeutet, dass das-Objekt vor einer Änderung dem Client eine Anforderung zur Berechtigung zum Ändern einer Eigenschaft sendet.</span><span class="sxs-lookup"><span data-stu-id="3710a-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="3710a-117">Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="3710a-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="3710a-118">Flags</span><span class="sxs-lookup"><span data-stu-id="3710a-118">Flags</span></span>

<span data-ttu-id="3710a-119">funcflag \_ frequestedit, varflag \_ frequestedit</span><span class="sxs-lookup"><span data-stu-id="3710a-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="3710a-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3710a-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="3710a-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3710a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3710a-122">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="3710a-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="3710a-123">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="3710a-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3710a-124">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="3710a-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3710a-125">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="3710a-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 