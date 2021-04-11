---
description: Enthält Informationen für die cryptuidlgviewsignerinfo-Funktion.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042252"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="e9a4e-103">Cryptui \_ viewsignerinfo- \_ Struktur Struktur</span><span class="sxs-lookup"><span data-stu-id="e9a4e-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="e9a4e-104">\[Die **cryptui \_ viewsignerinfo \_** -Struktur ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9a4e-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e9a4e-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e9a4e-106">Die **cryptui \_ viewsignerinfo \_** -Struktur Struktur enthält Informationen für die [**cryptuidlgviewsignerinfo**](cryptuidlgviewsignerinfo.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="e9a4e-107">Diese Struktur ist nicht in einer veröffentlichten Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="e9a4e-108">Um diese Struktur zu verwenden, deklarieren Sie Sie im exakten Format.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e9a4e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a4e-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="e9a4e-110">Member</span><span class="sxs-lookup"><span data-stu-id="e9a4e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9a4e-111">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-112">Die Größe (in Bytes) dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-113">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-114">Das Handle des Fensters, das als übergeordnetes Element des Dialog Felds angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="e9a4e-115">Dieser Member kann **null** sein, wenn das Dialogfeld kein übergeordnetes Element aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-117">Ein Satz von Flags, der das Verhalten der [**cryptuidlgviewsignerinfo**](cryptuidlgviewsignerinfo.md) -Funktion ändert.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="e9a4e-118">Zurzeit sind keine Flags definiert, daher muss dieser Member 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-119">**sztitle**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-120">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Titel enthält, der im Dialogfeld angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="e9a4e-121">Wenn dieser Member **null** ist, wird ein Standard Titel verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-122">**psignerinfo**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-123">Ein Zeiger auf eine [**CMSG- \_ Signatur Geber \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) -Struktur, die die anzuzeigenden Signatur Geber Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-124">**hmsg**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-125">Das Handle der Nachricht, aus der die Signatur Geber Informationen extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-126">**pszoid**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-127">Ein Zeiger auf eine mit NULL endende ANSI-Zeichenfolge, die die Zeichen folgen Darstellung des [*Objekt Bezeichners*](../secgloss/o-gly.md) (OID) enthält, der angibt, wofür das Zertifikat, das die Signatur durchgeführt hat, überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="e9a4e-128">Wenn diese z. b. aufgerufen wird, um die Signatur einer [*Zertifikat Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) anzuzeigen, sollte die **szoid \_ KP \_ CTL- \_ Verwendungs \_ Signatur** -OID-Zeichenfolge übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="e9a4e-129">Wenn dieser Member **null** ist, wird das Zertifikat nicht für die Verwendung überprüft.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-130">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-131">Dieser Parameter wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-131">This parameter is not currently used.</span></span> <span data-ttu-id="e9a4e-132">Dieser Member muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-133">**cstores**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-134">Die Anzahl der Elemente im **rghstores** -Array.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-135">**rghstores**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-136">Ein Array von **HCERTSTORE** -Werten, die die anderen Zertifikat Speicher für die Suche nach dem Zertifikat darstellen, mit dem die Nachricht signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="e9a4e-137">Wenn dieser Member **null** ist, werden keine weiteren Speicher durchsucht.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="e9a4e-138">Der **cstores** -Member enthält die Anzahl der Elemente in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-139">**cpropsheetpages**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-140">Die Anzahl der Elemente im **rgpropsheetpages** -Array.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="e9a4e-141">**rgpropsheetpages**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="e9a4e-142">Ein Array von [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur Zeigern, die alle zusätzlichen Seiten definieren, die im Standard Dialogfeld angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="e9a4e-143">Wenn dieser Member **null** ist, werden keine weiteren Seiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="e9a4e-144">Der **cpropsheetpages** -Member enthält die Anzahl der Elemente in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="e9a4e-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9a4e-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9a4e-145">Requirements</span></span>



| <span data-ttu-id="e9a4e-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9a4e-146">Requirement</span></span> | <span data-ttu-id="e9a4e-147">Wert</span><span class="sxs-lookup"><span data-stu-id="e9a4e-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a4e-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9a4e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a4e-149">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9a4e-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e9a4e-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9a4e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a4e-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9a4e-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9a4e-152">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e9a4e-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9a4e-153">**Cryptui \_ Viewsignerinfo \_ structw** (Unicode) und **cryptui \_ viewsignerinfo \_ Structa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9a4e-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9a4e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9a4e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a4e-155">**Cryptuidlgviewsignerinfo**</span><span class="sxs-lookup"><span data-stu-id="e9a4e-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
