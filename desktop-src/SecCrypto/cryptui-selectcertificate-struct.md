---
description: Enthält Informationen über das Dialogfeld, das von der cryptuidlgselectcertificate-Funktion angezeigt wird.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: CRYPTUI_SELECTCERTIFICATE_STRUCT Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355395"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="8a3b9-103">Cryptui \_ selectcertificate- \_ Struktur Struktur</span><span class="sxs-lookup"><span data-stu-id="8a3b9-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="8a3b9-104">Die **cryptui \_ selectcertificate \_** -Struktur Struktur enthält Informationen zu dem Dialogfeld, das von der [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) -Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a3b9-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="8a3b9-106">Member</span><span class="sxs-lookup"><span data-stu-id="8a3b9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a3b9-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-108">Die Größe (in Bytes) dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-109">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-110">Das Handle des übergeordneten Fensters des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="8a3b9-111">Wenn dieser Wert **null** ist, ist das übergeordnete Fenster das Standard Desktop Fenster.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-113">Gibt zusätzliche Optionen für die [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="8a3b9-114">Dies kann NULL oder ein bitweises **or** der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="8a3b9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8a3b9-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="8a3b9-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a3b9-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="8a3b9-117"><dt>**cryptui \_ selectcert \_ addfromds**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3b9-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="8a3b9-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="8a3b9-119"><dt>**cryptui \_ selectcert- \_ Legacy**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3b9-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="8a3b9-120">Gibt an, dass das Legacy Dialogfeld angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="8a3b9-121"><dt>**cryptui \_ selectcert \_ MultiSelect**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3b9-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="8a3b9-122">Ermöglicht es dem Benutzer, mehr als ein Zertifikat im Dialogfeld auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="8a3b9-123">Wenn dieses Flag festgelegt ist, gibt die Funktion [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) immer **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="8a3b9-124">Der **hselectedcertstore** -Member dieser Struktur muss ein Handle für einen Zertifikat Speicher enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="8a3b9-125">Die Zertifikate, die vom Benutzer ausgewählt werden, werden diesem Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="8a3b9-126"><dt>**cryptui \_ selectcert \_ Put \_ Window \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3b9-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="8a3b9-127">Erzwingt, dass die kryptografiebenutzeroberfläche das oberste Fenster auf dem Bildschirm ist.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="8a3b9-128">**sztitle**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-129">Der Anzeige Titel für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-129">The display title for the dialog box.</span></span> <span data-ttu-id="8a3b9-130">Wenn der Wert dieses Members **null** ist, wird der Standard Titel "Zertifikat auswählen" verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-131">**dwdontusecolumn**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-132">Flags, die kombiniert werden können, um Spalten der Anzeige auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="8a3b9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8a3b9-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="8a3b9-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a3b9-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="8a3b9-135"><dt>**Cryptui \_ \_IssuedTo- \_ Spalte**</dt> <dt>1 (0x1)</dt> auswählen</span><span class="sxs-lookup"><span data-stu-id="8a3b9-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="8a3b9-136">**IssuedTo** -Informationen nicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="8a3b9-137"><dt>**Cryptui \_ Select \_ IssuedBy \_ Spalte**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8a3b9-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="8a3b9-138">**IssuedBy** -Informationen nicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="8a3b9-139"><dt>**Cryptui \_ \_Intendeduse- \_ Spalte**</dt> <dt>4 (0x4)</dt> auswählen</span><span class="sxs-lookup"><span data-stu-id="8a3b9-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="8a3b9-140">Zeigen Sie keine **intendeduse** -Informationen an.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="8a3b9-141"><dt>**Cryptui \_ Wählen Sie \_ FriendlyName \_ Column**</dt> <dt>8 (0x8)</dt> aus.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="8a3b9-142">Zeigen Sie keine Namensinformationen an.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="8a3b9-143"><dt>**Cryptui \_ \_Location \_ Column**</dt> <dt>16 (0x10)</dt> auswählen</span><span class="sxs-lookup"><span data-stu-id="8a3b9-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="8a3b9-144">Zeigen Sie keine Standortinformationen an.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="8a3b9-145"><dt>**Cryptui \_ \_Ablauf \_ Spalte**</dt> <dt>32 (0x20)</dt> auswählen</span><span class="sxs-lookup"><span data-stu-id="8a3b9-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="8a3b9-146">Ablauf Informationen nicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="8a3b9-147">**szdisplaystring**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-148">Text, der im Dialogfeld angezeigt wird, um den Benutzer anzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="8a3b9-149">Wenn der Wert dieses Members **null** ist, wird die Standard Zeichenfolge "wählen Sie ein Zertifikat aus, das Sie verwenden möchten" verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-150">**pfiltercallback**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-151">Ein Zeiger auf eine [**pfncfilterproc**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) -Rückruffunktion, die die Zertifikate filtert, die im Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-152">**pdisplaycallback**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-153">Ein Zeiger auf eine [**pfnccertdisplayproc**](pfnccertdisplayproc.md) -Rückruffunktion, die Zertifikate anzeigt, die der Benutzer zum anzeigen auswählt.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-154">**pvcallbackdata**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-155">Zusätzliche Daten, die an die Rückruf Funktionen übergeben werden, die von den **pfiltercallback** -und **pdisplaycallback** -Membern angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-156">**cdisplaystores**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-157">Die Anzahl der Zertifikat Speicher im **rghdisplaystores** -Array.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-158">**rghdisplaystores**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-159">Ein Zeiger auf ein Array von Stores, die Zertifikate enthalten, die im Dialogfeld zur Auswahl stehen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-160">**cstores**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-161">Die Anzahl der Zertifikat Speicher im **rghstores** -Array.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-162">**rghstores**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-163">Ein Zeiger auf ein Array von Zertifikat speichern, das beim Aufbau einer Zertifikat Kette durchsucht werden soll, und das Überprüfen der Vertrauenswürdigkeit für die im Dialogfeld angezeigten Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-164">**cpropsheetpages**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-165">Die Anzahl der Eigenschaften Seiten im **rgpropsheetpages** -Array.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-166">**rgpropsheetpages**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-167">Ein Zeiger auf ein Array von **PROPSHEETPAGE** -Strukturen, die Eigenschaften Seiten darstellen, die an das Dialogfeld zum Anzeigen von Zertifikaten übermittelt werden, wenn ein Zertifikat für die Anzeige ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="8a3b9-168">**hselectedcertstore**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="8a3b9-169">Ein Handle für einen vom Aufrufer erstellten Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="8a3b9-170">Die vom Benutzer ausgewählten Zertifikate werden diesem Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="8a3b9-171">Wenn die Anzahl der Zertifikate in diesem Speicher vor und nach dem Aufruf von [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md)identisch ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="8a3b9-172">Dieser Member wird nicht verwendet, wenn der **dwFlags** -Member dieser Struktur das MultiSelect-Flag " **cryptui \_ selectcert \_** " nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="8a3b9-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a3b9-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a3b9-173">Requirements</span></span>



| <span data-ttu-id="8a3b9-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a3b9-174">Requirement</span></span> | <span data-ttu-id="8a3b9-175">Wert</span><span class="sxs-lookup"><span data-stu-id="8a3b9-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3b9-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a3b9-176">Minimum supported client</span></span><br/> | <span data-ttu-id="8a3b9-177">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a3b9-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="8a3b9-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a3b9-178">Minimum supported server</span></span><br/> | <span data-ttu-id="8a3b9-179">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a3b9-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8a3b9-180">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8a3b9-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a3b9-181">**Cryptui \_ Selectcertificate \_ structw** (Unicode) und **cryptui \_ selectcertificate \_ Structa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a3b9-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a3b9-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a3b9-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3b9-183">**Cryptuidlgselectcertificate**</span><span class="sxs-lookup"><span data-stu-id="8a3b9-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




