---
description: 'IWiaUIExtension::D eviceDialog-Methode: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standardsystembenutzeroberfläche ersetzt.'
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension::D eviceDialog-Methode (Wiadevd.h)
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
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116708"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="b5843-103">IWiaUIExtension::D eviceDialog-Methode</span><span class="sxs-lookup"><span data-stu-id="b5843-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="b5843-104">Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standardsystem-Benutzeroberfläche ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b5843-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5843-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5843-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="b5843-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5843-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5843-107">*pDeviceDialogData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b5843-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5843-108">Typ: **PDEVICEDIALOGDATA \***</span><span class="sxs-lookup"><span data-stu-id="b5843-108">Type: **PDEVICEDIALOGDATA\***</span></span>

<span data-ttu-id="b5843-109">Zeigt auf eine [**DEVICEDIALOGDATA-Struktur,**](-wia-devicedialogdata.md) die alle Daten enthält, die zum Implementieren des Gerätedialogs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b5843-109">Points to a [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5843-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5843-110">Return value</span></span>

<span data-ttu-id="b5843-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b5843-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b5843-112">Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5843-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b5843-113">Wenn der Benutzer den Dialog abbricht, gibt die Methode S \_ FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="b5843-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="b5843-114">Wenn die Methode nicht implementiert ist, wird E \_ NOTIMPL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5843-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="b5843-115">Wenn die Methode fehlschlägt, wird ein COM-Standardfehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5843-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5843-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5843-116">Remarks</span></span>

<span data-ttu-id="b5843-117">Wenn Sie die [**IWiaUIExtension-Schnittstelle**](-wia-iwiauiextension.md) implementieren und die Systembenutzerschnittstelle nicht ersetzen möchten, muss diese Methode weiterhin implementiert werden, sollte aber nur E \_ NOTIMPL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b5843-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5843-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5843-118">Requirements</span></span>



| <span data-ttu-id="b5843-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5843-119">Requirement</span></span> | <span data-ttu-id="b5843-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b5843-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b5843-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5843-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5843-122">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5843-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5843-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5843-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5843-124">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5843-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b5843-125">Header</span><span class="sxs-lookup"><span data-stu-id="b5843-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5843-126"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5843-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




