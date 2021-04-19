---
description: Gibt einen Befehl für ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 aus.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2::D evicecommand-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344456"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="6b06a-103">IWiaItem2::D evicecommand-Methode</span><span class="sxs-lookup"><span data-stu-id="6b06a-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="6b06a-104">Gibt einen Befehl für ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 aus.</span><span class="sxs-lookup"><span data-stu-id="6b06a-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b06a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b06a-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="6b06a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b06a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b06a-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b06a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b06a-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="6b06a-108">Type: **LONG**</span></span>

<span data-ttu-id="6b06a-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b06a-109">Currently unused.</span></span> <span data-ttu-id="6b06a-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6b06a-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b06a-111">*pcmdguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b06a-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b06a-112">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="6b06a-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="6b06a-113">Gibt den Befehl an, der an das WIA 2,0-Gerät gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b06a-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="6b06a-114">Weitere Informationen finden Sie unter [_ *WIA-Geräte Befehle* \*](-wia-wia-device-commands.md).</span><span class="sxs-lookup"><span data-stu-id="6b06a-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b06a-115">*ppIWiaItem2* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6b06a-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b06a-116">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6b06a-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="6b06a-117">Empfängt die Adresse eines Zeigers auf das [**IWiaItem2**](-wia-iwiaitem2.md) Element, das vom Befehl erstellt wurde (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="6b06a-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b06a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b06a-118">Return value</span></span>

<span data-ttu-id="6b06a-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6b06a-119">Type: **HRESULT**</span></span>

<span data-ttu-id="6b06a-120">Zusätzlich zu den Standard-COM-Fehlercodes kann die-Methode den folgenden Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6b06a-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="6b06a-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b06a-121">Return code</span></span>                                                                                       | <span data-ttu-id="6b06a-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b06a-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b06a-123"><dt>**E \_ cmdnotsupported**</dt></span><span class="sxs-lookup"><span data-stu-id="6b06a-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="6b06a-124">Der-Befehl ist nicht für die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle implementiert, für die die-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6b06a-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="6b06a-125">Der numerische Wert für diesen Fehler ist noch nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6b06a-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b06a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b06a-126">Remarks</span></span>

<span data-ttu-id="6b06a-127">Das Verhalten dieser Methode hängt von der Kategorie des Knotens ab, auf dem die Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6b06a-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="6b06a-128">Wenn die Anwendung mithilfe der **IWiaItem2::D evicecommand** -Methode den Befehl [**Bild von WIA \_ cmd über \_ nehmen \_**](-wia-wia-device-commands.md) an das Gerät sendet, erstellt das WIA 2,0-Laufzeitsystem ein [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt, das das Bild darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b06a-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="6b06a-129">Die **IWiaItem2::D evicecommand** -Methode speichert die Adresse der Schnittstelle im *ppIWiaItem2* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b06a-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="6b06a-130">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="6b06a-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b06a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b06a-131">Requirements</span></span>



| <span data-ttu-id="6b06a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b06a-132">Requirement</span></span> | <span data-ttu-id="6b06a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6b06a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b06a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b06a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6b06a-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b06a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6b06a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b06a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6b06a-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b06a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6b06a-138">Header</span><span class="sxs-lookup"><span data-stu-id="6b06a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b06a-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b06a-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b06a-140">IDL</span><span class="sxs-lookup"><span data-stu-id="6b06a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b06a-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b06a-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
