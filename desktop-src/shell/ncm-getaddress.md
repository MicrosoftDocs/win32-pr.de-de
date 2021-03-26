---
description: Gibt an, ob eine Netzwerkadresse einem angegebenen Typ und Format entspricht.
title: NCM_GETADDRESS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977880"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="9be11-103">NCM- \_ GetAddress-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9be11-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="9be11-104">Gibt an, ob eine Netzwerkadresse einem angegebenen Typ und Format entspricht.</span><span class="sxs-lookup"><span data-stu-id="9be11-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="9be11-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9be11-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be11-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9be11-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9be11-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9be11-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9be11-108">*PV* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9be11-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="9be11-109">Ein Zeiger auf eine <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> -Struktur zum Empfangen von Netzwerk Adressinformationen in der analysierten Form, wenn das Adressformat und der Typ im von *HWND* angegebenen Steuerelement überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9be11-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="9be11-110">Die aufrufenden Anwendung ist dafür verantwortlich, den Arbeitsspeicher für diese Struktur zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9be11-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be11-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9be11-111">Return value</span></span>

<span data-ttu-id="9be11-112">Gibt einen der folgenden Werte vom Typ **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="9be11-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="9be11-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9be11-113">Return code</span></span>                                                                                                | <span data-ttu-id="9be11-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9be11-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9be11-115"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9be11-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="9be11-116">Die aufrufenden Anwendung konnte eine [**NC- \_ Adress**](/windows/win32/api/shellapi/ns-shellapi-nc_address) Struktur nicht zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9be11-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="9be11-117"><dt>**Fehler \_ beim \_ Puffer.**</dt></span><span class="sxs-lookup"><span data-stu-id="9be11-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="9be11-118">Der Ausgabepuffer ist zu klein, um die analysierte Netzwerkadresse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9be11-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="9be11-119"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="9be11-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="9be11-120">Die Netzwerk Adress Zeichenfolge ist nicht von einem beliebigen Typ angegeben.</span><span class="sxs-lookup"><span data-stu-id="9be11-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="9be11-121"><dt>**Fehler \_ erfolgreich**</dt></span><span class="sxs-lookup"><span data-stu-id="9be11-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="9be11-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9be11-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="9be11-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9be11-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="9be11-124">Es gibt keine Adresse im Netzwerk Adress Steuerelement, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9be11-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="9be11-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9be11-125">Remarks</span></span>

<span data-ttu-id="9be11-126">Verwenden Sie die **NCM \_ GetAddress** -Nachricht, um eine Netzwerkadresse in einem Netzwerk Adress Steuerelement mit einer voreingestellten Netzwerkadresse zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9be11-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="9be11-127">Verwenden Sie zum Instanziieren die in shellapi. h definierte Klasse **msctls- \_ netaddress** .</span><span class="sxs-lookup"><span data-stu-id="9be11-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="9be11-128">Ruft vor dem Senden dieser Nachricht [**initnetworkaddresscontrol**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf.</span><span class="sxs-lookup"><span data-stu-id="9be11-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="9be11-129">Dadurch wird die Bibliothek der allgemeinen Steuerelemente initialisiert, die das Netzwerk Adress Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="9be11-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="9be11-130">Diese Nachricht Ruft die Netzwerk Adress Zeichenfolge aus einem Netzwerk Adress Steuerelement ab, analysiert die Zeichenfolge und überprüft, ob die Zeichenfolge mit einer Netzwerk Adresstyp Maske übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9be11-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="9be11-131">Wenn die Zeichenfolge mit der Maske übereinstimmt, gibt die Meldung S \_ OK zurück und gibt die Zeichenfolge in der analysierten Form an die aufrufende Anwendung zurück (einschließlich der Portnummer, der Präfix Länge und anderer Adressinformationen), wobei die [**NC- \_ Adress**](/windows/win32/api/shellapi/ns-shellapi-nc_address) Struktur verwendet wird, auf die von *PV* verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="9be11-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="9be11-132">Diese Meldung gibt E \_ invalidArg zurück, wenn die aufrufende Anwendung die Struktur nicht zuordnen kann, auf die von *PV* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9be11-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="9be11-133">Darstellungen von IP-Adressen (Internet Protocol), Version 4 und 6 (V4/V6) für Dienste und Netzwerke sowie benannte Internet Adressen und Dienste mit Domain Name System-Format (DNS) werden analysiert.</span><span class="sxs-lookup"><span data-stu-id="9be11-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="9be11-134">Wenn die Netzwerk Adress Zeichenfolge einen benannten Hostnamen (DNS) oder Dienst darstellt, ist der Wert, der im **prefixlength** -Member der [**NC- \_ Adresse**](/windows/win32/api/shellapi/ns-shellapi-nc_address) zurückgegeben wird, 0 (null)</span><span class="sxs-lookup"><span data-stu-id="9be11-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="9be11-135">Legen Sie den Netzwerk Adressentyp Mask mithilfe der [**NCM \_ setallowtype**](ncm-setallowtype.md) -Nachricht fest, bevor Sie das **NCM- \_ GetAddress** -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="9be11-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="9be11-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9be11-136">Requirements</span></span>



| <span data-ttu-id="9be11-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9be11-137">Requirement</span></span> | <span data-ttu-id="9be11-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9be11-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9be11-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9be11-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9be11-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9be11-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9be11-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9be11-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9be11-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9be11-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9be11-143">Header</span><span class="sxs-lookup"><span data-stu-id="9be11-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be11-144"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9be11-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be11-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9be11-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be11-146">**NCM- \_ getallowtype**</span><span class="sxs-lookup"><span data-stu-id="9be11-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="9be11-147">**NETADDR- \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="9be11-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




