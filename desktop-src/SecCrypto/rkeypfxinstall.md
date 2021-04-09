---
description: Die rkeypfxinstall-Funktion wird nicht unterstützt.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Rkeypfxinstall-Funktion (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958945"
---
# <a name="rkeypfxinstall-function"></a>Rkeypfxinstall-Funktion

Die **rkeypfxinstall** -Funktion wird nicht unterstützt.

**Windows Server 2003:** Die **rkeypfxinstall** -Funktion installiert ein Zertifikat auf einem Remote Computer. Beachten Sie, dass sich dieses Verhalten in Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.

## <a name="syntax"></a>Syntax


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hkeysvccli* \[ in\]
</dt> <dd>

Ein [**keysvcc \_ handle**](keysvcc-handle.md) -handle, das zuvor von [**rkeyopenkeyservice**](rkeyopenkeyservice.md)geöffnet wurde. Das Handle stellt den Remote Computer dar, von dem das Zertifikat empfangen wird. Dieser Wert darf nicht **null** sein.

</dd> <dt>

*ppfx* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**keysvc- \_ BLOB**](keysvc-blob.md) -Struktur, die das zu installierendes Zertifikat darstellt. Das BLOB weist das [*PKCS \# 12*](../secgloss/p-gly.md) -Format auf.

</dd> <dt>

*pPassword* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**keysvc- \_ Unicode- \_ Zeichen**](keysvc-unicode-string.md) folgen Struktur, die das Kennwort für das BLOB darstellt. Wenn Sie die Verwendung des Kennworts abgeschlossen haben, löschen Sie das Kennwort aus dem Arbeitsspeicher, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen. Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter [Handling Kennwörter](../secbp/handling-passwords.md).

</dd> <dt>

*ulflags* \[ in\]
</dt> <dd>

Flags, die die Installationsoptionen für Zertifikate angeben. Dieser Parameter kann eine NULL-oder eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**Crypt \_ Exportierbar**</dt><dt></dt> </dl>              | Importierte Schlüssel werden als exportierbar markiert.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**Crypt \_ Computer- \_ Keyset**</dt><dt></dt> </dl> | Private Schlüssel werden auf dem Remote Computer und nicht unter dem aktuellen Benutzer gespeichert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ulong** -Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rkeyclosekeyservice**](rkeyclosekeyservice.md)
</dt> <dt>

[**Rkeyopenkeyservice**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
