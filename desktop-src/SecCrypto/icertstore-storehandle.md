---
description: Legt das HCERTSTORE-Handle eines Zertifikat Speicher fest oder ruft es ab.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Icertstore:: StoreHandle-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364731"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="7a398-103">Icertstore:: StoreHandle-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a398-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="7a398-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="7a398-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="7a398-105">Die **storeHandle** -Eigenschaft legt das HCERTSTORE-Handle eines Zertifikat Speicher fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="7a398-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="7a398-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7a398-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a398-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a398-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="7a398-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7a398-108">Property value</span></span>

<span data-ttu-id="7a398-109">Das HCERTSTORE-Handle des Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="7a398-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a398-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7a398-110">Error codes</span></span>

<span data-ttu-id="7a398-111">Wenn die Eigenschaften Zugriffsmethoden **" \_ storeHandle** " und " **\_ storeHandle** " erfolgreich sind, geben Sie "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="7a398-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="7a398-112">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7a398-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a398-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a398-113">Remarks</span></span>

<span data-ttu-id="7a398-114">Zum Freigeben des Kontexts muss entweder die [**CloseHandle**](icertstore-closehandle.md) -Methode oder die [**certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) -Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a398-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="7a398-115">Wenn Sie die **storeHandle** -Eigenschaft festlegen, wird der Status des gesamten [**Speicher**](store.md) Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a398-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a398-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a398-116">Requirements</span></span>



| <span data-ttu-id="7a398-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a398-117">Requirement</span></span> | <span data-ttu-id="7a398-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7a398-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a398-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7a398-119">Redistributable</span></span><br/> | <span data-ttu-id="7a398-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a398-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7a398-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7a398-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="7a398-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a398-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a398-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a398-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a398-124">**Icertstore**</span><span class="sxs-lookup"><span data-stu-id="7a398-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




