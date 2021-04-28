---
description: 'IWiaUIExtension2::D eviceDialog-Methode: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standardsystem-Benutzeroberfläche ersetzt.'
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2::D eviceDialog-Methode (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116648"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="9abc7-103">IWiaUIExtension2::D eviceDialog-Methode</span><span class="sxs-lookup"><span data-stu-id="9abc7-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="9abc7-104">Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standard-Benutzeroberfläche des Systems ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9abc7-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9abc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9abc7-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="9abc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9abc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9abc7-107">*pDeviceDialogData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9abc7-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9abc7-108">Typ: **PDEVICEDIALOGDATA2 \***</span><span class="sxs-lookup"><span data-stu-id="9abc7-108">Type: **PDEVICEDIALOGDATA2\***</span></span>

<span data-ttu-id="9abc7-109">Verweist auf eine [**DEVICEDIALOGDATA2-Struktur,**](-wia-devicedialogdata2.md) die alle Daten enthält, die zum Implementieren des Gerätedialogs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9abc7-109">Points to a [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9abc7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9abc7-110">Return value</span></span>

<span data-ttu-id="9abc7-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9abc7-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9abc7-112">Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9abc7-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="9abc7-113">Wenn der Benutzer den Dialog abbricht, gibt die Methode S \_ FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="9abc7-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="9abc7-114">Wenn bei der Methode ein Fehler auftritt, wird ein entsprechender Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9abc7-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="9abc7-115">Die folgende Tabelle zeigt einige der möglichen Rückgabestatuscodes.</span><span class="sxs-lookup"><span data-stu-id="9abc7-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="9abc7-116">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="9abc7-116">Error code</span></span>    | <span data-ttu-id="9abc7-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9abc7-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="9abc7-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9abc7-118">E\_INVALIDARG</span></span> | <span data-ttu-id="9abc7-119">Der Parameter pDeviceDialogData ist **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9abc7-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="9abc7-120">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="9abc7-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="9abc7-121">Die Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9abc7-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="9abc7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9abc7-122">Remarks</span></span>

<span data-ttu-id="9abc7-123">Wenn Sie die [**IWiaUIExtension2-Schnittstelle**](-wia-iwiauiextension2.md) implementieren und die Systemoberfläche nicht ersetzen möchten, muss diese Methode weiterhin implementiert werden, sollte aber nur E \_ NOTIMPL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9abc7-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abc7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9abc7-124">Requirements</span></span>



| <span data-ttu-id="9abc7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9abc7-125">Requirement</span></span> | <span data-ttu-id="9abc7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9abc7-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9abc7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9abc7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9abc7-128">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9abc7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9abc7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9abc7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9abc7-130">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9abc7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9abc7-131">Header</span><span class="sxs-lookup"><span data-stu-id="9abc7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9abc7-132"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="9abc7-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




