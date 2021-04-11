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
# <a name="other-session-constants"></a>Andere Sitzungs Konstanten

Konstanten, die in der folgenden Liste aufgeführt sind, in der **\_ \_ wsmansessionflags** -Enumeration, die den Port für Codierung, Verschlüsselung und Dienst Prinzipal Name angeben.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Sendet die Anforderung in UTF8 anstelle von UTF16.

Die zugeordnete Skript Methode ist [**WSMAN. SessionFlagUTF8**](wsman-sessionflagutf8.md) und die C++-Methode ist [**iwsmanex. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**Wsmanflagnoencryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Verschlüsseln Sie die über das Netzwerk gesendeten Nachrichten nicht. Diese Einstellung ist nur zulässig, wenn der [*Listener*](windows-remote-management-glossary.md) so konfiguriert ist, dass " **zugwunverschlüsselt** " auf " **true**" festgelegt ist.

Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagnoencryption**](wsman-sessionflagnoencryption.md) ", und die C++-Methode ist " [**iwsmanex. sessionflagnoencryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**Wsmanflagenablespnserverport**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Geben Sie den Dienst Prinzipal Namen (SPN) an, wenn Sie eine direkte Verbindung mit der Remote BMC-Hardware herstellen, die auch als [*out-of-Band-*](windows-remote-management-glossary.md) Verbindung bezeichnet wird. Da sowohl der WinRM-Server Computer als auch die BMC-Hardware dieselbe IP-Adresse gemeinsam verwenden können, gibt dieses Flag an, dass die SPN-Portnummer verwendet werden muss, um zu bestimmen, ob die Verbindung mit dem Dienst oder direkt mit dem BMC hergestellt werden soll. Weitere Informationen finden Sie unter [namens Formate für eindeutige SPNs](/windows/desktop/AD/name-formats-for-unique-spns).

Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagenablespnserverport**](wsman-sessionflagenablespnserverport.md) , und die C++-Methode ist [**iwsmanex. sessionflagenablespnserverport**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



Sendet die Anforderung in UTF16.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Sitzungs Konstanten](session-constants.md)
</dt> </dl>

 

