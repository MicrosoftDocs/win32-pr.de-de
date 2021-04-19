---
description: Die rkeyopenkeyservice-Funktion wird nicht unterstützt.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Rkeyopenkeyservice-Funktion (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348729"
---
# <a name="rkeyopenkeyservice-function"></a>Rkeyopenkeyservice-Funktion

Die **rkeyopenkeyservice** -Funktion wird nicht unterstützt.

**Windows Server 2003:** Die **rkeyopenkeyservice** -Funktion stellt eine Verbindung mit einem Remote Computer her und öffnet ein Schlüsseldienst handle. Das Schlüsseldienst Handle kann anschließend von der Funktion [**rkeypfxinstall**](rkeypfxinstall.md) verwendet werden. Beachten Sie, dass sich dieses Verhalten in Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.

## <a name="syntax"></a>Syntax


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszmachinename* \[ in\]
</dt> <dd>

Langer Zeiger auf eine auf NULL endende Zeichenfolge, die den Computer darstellt, auf dem das Schlüsseldienst Handle geöffnet wird.

</dd> <dt>

*Besitztyp* \[ in\]
</dt> <dd>

[**Keysvc \_ Der Typwert**](keysvc-type.md) , der den Schlüsseltyp darstellt. Der einzige unterstützte Wert ist " **keysvcmachine**".

</dd> <dt>

*pwszownername* \[ in\]
</dt> <dd>

Reserviert. Legen Sie diesen Wert auf **null** fest.

</dd> <dt>

*pauthentication* \[ in\]
</dt> <dd>

Ein Zeiger auf ein **void** -, das die Authentifizierungs Einstellungen darstellt. Dieser Zeiger kann auf einen Wert von 0 (null) oder auf den folgenden Wert zeigen.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <dt>**Rkeysvc \_ \_ \_ nur sichere Verbindung herstellen**</dt><dt></dt> </dl> | Für den Client ist eine gegenseitige Authentifizierung erforderlich. Wenn dieser Wert angegeben wird, tritt ein Fall Back auf NTLM auf.<br/> |



 

</dd> <dt>

*beibehalten* \[ in, out\]
</dt> <dd>

Reserviert. Legen Sie diesen Wert auf **null** fest.

</dd> <dt>

*phkeysvccli* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein [**keysvcc- \_ handle**](keysvcc-handle.md) , das das geöffnete Schlüsseldienst handle empfängt. Wenn Sie die Verwendung des Handles abgeschlossen haben, können Sie die Ressource freigeben, indem Sie die [**rkeyclosekeyservice**](rkeyclosekeyservice.md) -Funktion aufrufen.

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

[**Rkeypfxinstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




