---
description: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2::D evicedialog-Methode (wiadevd. h)
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
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214649"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="aba67-103">IWiaUIExtension2::D evicedialog-Methode</span><span class="sxs-lookup"><span data-stu-id="aba67-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="aba67-104">Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.</span><span class="sxs-lookup"><span data-stu-id="aba67-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aba67-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="aba67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aba67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba67-107">*pdevicedialogdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aba67-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba67-108">Typ: \**PDEVICEDIALOGDATA2 \** _</span><span class="sxs-lookup"><span data-stu-id="aba67-108">Type: \**PDEVICEDIALOGDATA2\** _</span></span>

<span data-ttu-id="aba67-109">Verweist auf eine [_ *DEVICEDIALOGDATA2* \*](-wia-devicedialogdata2.md) -Struktur, die alle Daten enthält, die zum Implementieren des Geräte Dialogfelds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="aba67-109">Points to a [_ *DEVICEDIALOGDATA2*\*](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aba67-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aba67-110">Return value</span></span>

<span data-ttu-id="aba67-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aba67-111">Type: **HRESULT**</span></span>

<span data-ttu-id="aba67-112">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="aba67-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="aba67-113">Wenn der Benutzer das Dialogfeld abbricht, gibt die Methode den Wert "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="aba67-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="aba67-114">Wenn die Methode fehlschlägt, wird ein entsprechender Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aba67-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="aba67-115">In der folgenden Tabelle sind einige der möglichen Rückgabestatus Codes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="aba67-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="aba67-116">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="aba67-116">Error code</span></span>    | <span data-ttu-id="aba67-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aba67-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="aba67-118">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="aba67-118">E\_INVALIDARG</span></span> | <span data-ttu-id="aba67-119">Pdevicedialogdata des Parameters ist **null**.</span><span class="sxs-lookup"><span data-stu-id="aba67-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="aba67-120">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="aba67-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="aba67-121">Die Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="aba67-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="aba67-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aba67-122">Remarks</span></span>

<span data-ttu-id="aba67-123">Wenn Sie die [**IWiaUIExtension2**](-wia-iwiauiextension2.md) -Schnittstelle implementieren und die Systembenutzer Oberfläche nicht ersetzen möchten, muss diese Methode trotzdem implementiert werden, aber Sie sollte nicht mehr als "E \_ notimpl" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aba67-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba67-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aba67-124">Requirements</span></span>



| <span data-ttu-id="aba67-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aba67-125">Requirement</span></span> | <span data-ttu-id="aba67-126">Wert</span><span class="sxs-lookup"><span data-stu-id="aba67-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aba67-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aba67-127">Minimum supported client</span></span><br/> | <span data-ttu-id="aba67-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aba67-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aba67-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aba67-129">Minimum supported server</span></span><br/> | <span data-ttu-id="aba67-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aba67-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aba67-131">Header</span><span class="sxs-lookup"><span data-stu-id="aba67-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="aba67-132"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba67-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




