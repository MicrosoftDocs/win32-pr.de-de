---
title: readonly-Attribut
description: Das Attribut \ schreibgeschützt \ untersagt die Zuweisung zu einer Variablen.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- Schreib geschütztes Attribut, Mittel l
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948692"
---
# <a name="readonly-attribute"></a><span data-ttu-id="bcc93-104">readonly-Attribut</span><span class="sxs-lookup"><span data-stu-id="bcc93-104">readonly attribute</span></span>

<span data-ttu-id="bcc93-105">Das **Schreib \[ geschützte Attribut verhindert die Zuweisung zu einer Variablen. \]**</span><span class="sxs-lookup"><span data-stu-id="bcc93-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="bcc93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcc93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc93-107">*optionale Attribute*</span><span class="sxs-lookup"><span data-stu-id="bcc93-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="bcc93-108">NULL oder mehr mittlere Attribute.</span><span class="sxs-lookup"><span data-stu-id="bcc93-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="bcc93-109">*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="bcc93-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="bcc93-110">Der Typ der Daten, die im *Bezeichner* enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bcc93-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="bcc93-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="bcc93-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="bcc93-112">Ein Name, mit dem die Software auf den Daten Speicherort verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="bcc93-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcc93-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcc93-113">Remarks</span></span>

<span data-ttu-id="bcc93-114">Das **Schreib \[ geschützte Attribut verhindert die Zuweisung zu einer Variablen. \]**</span><span class="sxs-lookup"><span data-stu-id="bcc93-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="bcc93-115">"schreibgeschützt" wird nur auf Parameter Ebene, nicht auf Methoden Ebene unterstützt. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="bcc93-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="bcc93-116">Flags</span><span class="sxs-lookup"><span data-stu-id="bcc93-116">Flags</span></span>

<span data-ttu-id="bcc93-117">varflag \_ freadonly</span><span class="sxs-lookup"><span data-stu-id="bcc93-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="bcc93-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcc93-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="bcc93-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bcc93-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc93-120">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="bcc93-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="bcc93-121">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="bcc93-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="bcc93-122">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="bcc93-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="bcc93-123">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="bcc93-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 