---
description: Die RKeyPFXInstall-Funktion wird nicht unterstützt.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: RKeyPFXInstall-Funktion (Rkeysvcc.h)
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
ms.openlocfilehash: f19a01e9132bf9c4b1e281a75b0e0d7a27b4f9c7f299eefdd47bef8d60daea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900545"
---
# <a name="rkeypfxinstall-function"></a>RKeyPFXInstall-Funktion

Die **RKeyPFXInstall-Funktion** wird nicht unterstützt.

**Windows Server 2003:** Die **RKeyPFXInstall-Funktion** installiert ein Zertifikat auf einem Remotecomputer. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.

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

*hKeySvcCli* \[ In\]
</dt> <dd>

Ein [**KEYSVCC \_ HANDLE-Handle,**](keysvcc-handle.md) das zuvor von [**RKeyOpenKeyService geöffnet wurde.**](rkeyopenkeyservice.md) Das Handle stellt den Remotecomputer dar, der das Zertifikat erhält. Dieser Wert darf nicht **NULL sein.**

</dd> <dt>

*pPFX* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**KEYSVC-BLOB-Struktur, \_**](keysvc-blob.md) die das zu installierende Zertifikat darstellt. Das BLOB hat das [*PKCS \# 12-Format.*](../secgloss/p-gly.md)

</dd> <dt>

*pPassword* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**KEYSVC \_ UNICODE \_ STRING-Struktur,**](keysvc-unicode-string.md) die das Kennwort für das BLOB darstellt. Wenn Sie die Verwendung des Kennworts abgeschlossen haben, löschen Sie das Kennwort aus dem Arbeitsspeicher, indem Sie die [**SecureZeroMemory-Funktion**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) aufrufen. Weitere Informationen zum Schutz von Kennwörtern finden Sie unter [Behandeln von Kennwörtern.](../secbp/handling-passwords.md)

</dd> <dt>

*ulFlags* \[ In\]
</dt> <dd>

Flags, die die Zertifikatinstallationsoptionen angeben. Dieser Parameter kann eine Null oder eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**CRYPT \_ EXPORTIERBAR**</dt><dt></dt> </dl>              | Importierte Schlüssel werden als exportierbar markiert.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**CRYPT \_ MACHINE \_ KEYSET**</dt><dt></dt> </dl> | Private Schlüssel werden auf dem Remotecomputer und nicht unter dem aktuellen Benutzer gespeichert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ULONG-Wert,** der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
