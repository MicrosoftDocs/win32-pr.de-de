---
description: Die mxdc \_ XPS \_ S0PAGE \_ Resource \_ T-Struktur enthält Informationen über eine Ressource, z. b. ein Bild oder eine Schriftart, die einer XPS-Dokument Seite zugeordnet ist und an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei übermittelt werden soll.
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865871"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="f35e8-103">Mxdc \_ XPS \_ S0PAGE \_ Resource \_ T-Struktur</span><span class="sxs-lookup"><span data-stu-id="f35e8-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="f35e8-104">Die **mxdc \_ XPS \_ S0PAGE \_ Resource \_ T** -Struktur enthält Informationen über eine Ressource, z. b. ein Bild oder eine Schriftart, die einer XPS-Dokument Seite zugeordnet ist und an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f35e8-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f35e8-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="f35e8-106">Member</span><span class="sxs-lookup"><span data-stu-id="f35e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f35e8-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="f35e8-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="f35e8-108">Die Gesamtgröße dieser Struktur und der Ressource, auf die Sie verweist.</span><span class="sxs-lookup"><span data-stu-id="f35e8-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="f35e8-109">**dwresourcetype**</span><span class="sxs-lookup"><span data-stu-id="f35e8-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="f35e8-110">Ein Wert vom Typ [**mxdc \_ S0 \_ - \_ Seiten**](mxdcs0pageenums.md) Enumerationswerte, die den Typ der Ressource angeben, z. b. TIFF-Bild oder TrueType-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="f35e8-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="f35e8-111">**szuri**</span><span class="sxs-lookup"><span data-stu-id="f35e8-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="f35e8-112">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f35e8-112">The URI of the resource.</span></span> <span data-ttu-id="f35e8-113">Dies darf nicht mehr als 260 Bytes betragen.</span><span class="sxs-lookup"><span data-stu-id="f35e8-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f35e8-114">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="f35e8-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="f35e8-115">Die Größe der Ressource in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f35e8-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f35e8-116">**bData**</span><span class="sxs-lookup"><span data-stu-id="f35e8-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="f35e8-117">Die Daten der Ressource in einem Bytearray mit einer Größe von 1 + der Größe der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f35e8-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f35e8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f35e8-118">Remarks</span></span>

<span data-ttu-id="f35e8-119">Diese Struktur wird an eine [**mxdc- \_ Escape- \_ Header- \_ t**](mxdcescapeheader.md) -Struktur angehängt (deren **Opcode** auf **mxdcop \_ Set \_ S0PAGERESOURCE** festgelegt ist), um eine [**mxdc \_ S0PAGE \_ Resource Escape- \_ \_ t**](mxdcs0pageresourceescape.md) -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f35e8-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="f35e8-120">Die resultierende **mxdc \_ S0PAGE \_ Resource \_ Escape- \_ T** -Struktur wird dann im *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, die mit dem Escapezeichen " [**mxdc \_**](mxdc-escape.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f35e8-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="f35e8-121">Der Effekt besteht darin, die Ressource für die Konvertierung an den mxdc zu senden und in die Ausgabedatei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f35e8-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="f35e8-122">Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von " [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage);" liegen. Es können jedoch mehrere derartige Aufrufe zwischen den Aufrufen von **Startpage** und **EndPage** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f35e8-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="f35e8-123">Der Streamingverbrauch ist effizienter, wenn [**Sie extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem **mxdcop \_ Set \_ S0PAGE \_ Resource** **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie **extescape** mit dem **mxdcop \_ Set \_ S0PAGE** **Opcode** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="f35e8-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f35e8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f35e8-124">Requirements</span></span>



| <span data-ttu-id="f35e8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f35e8-125">Requirement</span></span> | <span data-ttu-id="f35e8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f35e8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f35e8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f35e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f35e8-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f35e8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f35e8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f35e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f35e8-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f35e8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f35e8-131">Header</span><span class="sxs-lookup"><span data-stu-id="f35e8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f35e8-132"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f35e8-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f35e8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f35e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35e8-134">Drucken</span><span class="sxs-lookup"><span data-stu-id="f35e8-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f35e8-135">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f35e8-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="f35e8-136">[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f35e8-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f35e8-137">**Extescape**</span><span class="sxs-lookup"><span data-stu-id="f35e8-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="f35e8-138">**mxdc-Escapezeichen \_**</span><span class="sxs-lookup"><span data-stu-id="f35e8-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

