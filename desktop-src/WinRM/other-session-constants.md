---
title: Andere Sitzungskonstanten (WSManDisp.h)
description: Geben Sie Codierung, Verschlüsselung und Dienstprinzipalnamenport an.
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
ms.openlocfilehash: fcd9d2cf44063dfb1a7ec1bfcbb0fe785d1747d34e84ef2c2d8c78598e6e6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743325"
---
# <a name="other-session-constants"></a>Andere Sitzungskonstanten

Konstanten, die in der folgenden Liste aufgeführt sind, in der **\_ \_ WSManSessionFlags-Enumeration,** die Codierung, Verschlüsselung und Dienstprinzipalnamenport angeben.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Sendet die Anforderung in UTF8 anstelle von UTF16.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagUTF8,**](wsman-sessionflagutf8.md) und die C++-Methode ist [**IWSManEx.SessionFlagUTF8.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Verschlüsseln Sie die über das Netzwerk gesendeten Nachrichten nicht. Diese Einstellung ist nur zulässig, wenn der [*Listener*](windows-remote-management-glossary.md) so konfiguriert ist, dass **AllowUnencrypted** auf **True** festgelegt ist.

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagNoEncryption,**](wsman-sessionflagnoencryption.md) und die C++-Methode ist [**IWSManEx.SessionFlagNoEncryption.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Geben Sie den SPN-Port (Service Principal Name) an, wenn Sie eine direkte Verbindung mit BMC-Remotehardware herstellen, die auch als [*Out-of-Band-Verbindung*](windows-remote-management-glossary.md) bezeichnet wird. Da sowohl der WinRM-Servercomputer als auch die BMC-Hardware dieselbe IP-Adresse gemeinsam verwenden können, gibt dieses Flag an, dass die SPN-Portnummer verwendet werden muss, um zu bestimmen, ob die Verbindung mit dem Dienst oder direkt mit dem BMC hergestellt wird. Weitere Informationen finden Sie unter [Namensformate für eindeutige SPNs.](/windows/desktop/AD/name-formats-for-unique-spns)

Die zugeordnete Skriptmethode ist [**WSMan.SessionFlagEnableSPNServerPort,**](wsman-sessionflagenablespnserverport.md) und die C++-Methode ist [**IWSManEx.SessionFlagEnableSPNServerPort.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Sitzungskonstanten](session-constants.md)
</dt> </dl>

 

