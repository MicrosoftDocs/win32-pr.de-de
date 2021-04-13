---
description: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Iwiauiextension::D evicedialog-Methode (wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526447"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="0d1d2-103">Iwiauiextension::D evicedialog-Methode</span><span class="sxs-lookup"><span data-stu-id="0d1d2-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="0d1d2-104">Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0d1d2-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d1d2-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="0d1d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d1d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1d2-107">*pdevicedialogdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d1d2-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d1d2-108">Typ: \**pdevicedialogdata \** _</span><span class="sxs-lookup"><span data-stu-id="0d1d2-108">Type: \**PDEVICEDIALOGDATA\** _</span></span>

<span data-ttu-id="0d1d2-109">Verweist auf eine [_ *devicedialogdata* \*](-wia-devicedialogdata.md) -Struktur, die alle Daten enthält, die zum Implementieren des Geräte Dialogfelds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0d1d2-109">Points to a [_ *DEVICEDIALOGDATA*\*](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d1d2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d1d2-110">Return value</span></span>

<span data-ttu-id="0d1d2-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d1d2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="0d1d2-112">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="0d1d2-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="0d1d2-113">Wenn der Benutzer das Dialogfeld abbricht, gibt die Methode den Wert "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="0d1d2-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="0d1d2-114">Wenn die Methode nicht implementiert ist, wird E \_ notimpl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d1d2-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="0d1d2-115">Wenn die Methode fehlschlägt, wird ein Standard-com-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d1d2-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d1d2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d1d2-116">Remarks</span></span>

<span data-ttu-id="0d1d2-117">Wenn Sie die [**iwiauiextension**](-wia-iwiauiextension.md) -Schnittstelle implementieren und die Systembenutzer Oberfläche nicht ersetzen möchten, muss diese Methode trotzdem implementiert werden. Sie sollte jedoch nichts weiter tun, als "E \_ notimpl" zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0d1d2-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1d2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d1d2-118">Requirements</span></span>



| <span data-ttu-id="0d1d2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d1d2-119">Requirement</span></span> | <span data-ttu-id="0d1d2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0d1d2-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1d2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d1d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1d2-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d1d2-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0d1d2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d1d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1d2-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d1d2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0d1d2-125">Header</span><span class="sxs-lookup"><span data-stu-id="0d1d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1d2-126"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1d2-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




