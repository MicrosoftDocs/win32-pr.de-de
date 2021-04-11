---
title: Andere Sitzungs Konstanten (WSManDisp. h)
description: Geben Sie den Port für Codierung, Verschlüsselung und Dienst Prinzipal Name an.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105632"
---
# <a name="other-session-constants"></a><span data-ttu-id="ac273-103">Andere Sitzungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="ac273-103">Other Session Constants</span></span>

<span data-ttu-id="ac273-104">Konstanten, die in der folgenden Liste aufgeführt sind, in der **\_ \_ wsmansessionflags** -Enumeration, die den Port für Codierung, Verschlüsselung und Dienst Prinzipal Name angeben.</span><span class="sxs-lookup"><span data-stu-id="ac273-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="ac273-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="ac273-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac273-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ac273-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="ac273-107">Sendet die Anforderung in UTF8 anstelle von UTF16.</span><span class="sxs-lookup"><span data-stu-id="ac273-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="ac273-108">Die zugeordnete Skript Methode ist [**WSMAN. SessionFlagUTF8**](wsman-sessionflagutf8.md) und die C++-Methode ist [**iwsmanex. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span><span class="sxs-lookup"><span data-stu-id="ac273-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac273-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**Wsmanflagnoencryption**</span><span class="sxs-lookup"><span data-stu-id="ac273-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac273-110">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="ac273-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="ac273-111">Verschlüsseln Sie die über das Netzwerk gesendeten Nachrichten nicht.</span><span class="sxs-lookup"><span data-stu-id="ac273-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="ac273-112">Diese Einstellung ist nur zulässig, wenn der [*Listener*](windows-remote-management-glossary.md) so konfiguriert ist, dass " **zugwunverschlüsselt** " auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac273-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="ac273-113">Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagnoencryption**](wsman-sessionflagnoencryption.md) ", und die C++-Methode ist " [**iwsmanex. sessionflagnoencryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)".</span><span class="sxs-lookup"><span data-stu-id="ac273-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac273-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**Wsmanflagenablespnserverport**</span><span class="sxs-lookup"><span data-stu-id="ac273-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac273-115">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="ac273-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="ac273-116">Geben Sie den Dienst Prinzipal Namen (SPN) an, wenn Sie eine direkte Verbindung mit der Remote BMC-Hardware herstellen, die auch als [*out-of-Band-*](windows-remote-management-glossary.md) Verbindung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ac273-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="ac273-117">Da sowohl der WinRM-Server Computer als auch die BMC-Hardware dieselbe IP-Adresse gemeinsam verwenden können, gibt dieses Flag an, dass die SPN-Portnummer verwendet werden muss, um zu bestimmen, ob die Verbindung mit dem Dienst oder direkt mit dem BMC hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac273-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="ac273-118">Weitere Informationen finden Sie unter [namens Formate für eindeutige SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span><span class="sxs-lookup"><span data-stu-id="ac273-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="ac273-119">Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagenablespnserverport**](wsman-sessionflagenablespnserverport.md) , und die C++-Methode ist [**iwsmanex. sessionflagenablespnserverport**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span><span class="sxs-lookup"><span data-stu-id="ac273-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac273-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="ac273-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac273-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="ac273-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="ac273-122">Sendet die Anforderung in UTF16.</span><span class="sxs-lookup"><span data-stu-id="ac273-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac273-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac273-123">Requirements</span></span>



| <span data-ttu-id="ac273-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac273-124">Requirement</span></span> | <span data-ttu-id="ac273-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ac273-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac273-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac273-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac273-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac273-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ac273-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac273-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac273-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac273-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ac273-130">Header</span><span class="sxs-lookup"><span data-stu-id="ac273-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac273-131"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac273-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac273-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ac273-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac273-133"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac273-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac273-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac273-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac273-135">Sitzungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="ac273-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

