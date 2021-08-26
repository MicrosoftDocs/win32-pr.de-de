---
description: Gibt den bevorzugten Authentifizierungstokentyp für den Endpunkt des Diensts zurück.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType-Methode (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a9b7d15d6d27170106118c720d25567389884c50e27aac202adedf00290236c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994580"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType-Methode

Gibt den bevorzugten Authentifizierungstokentyp für den Endpunkt des Diensts zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*serviceId* \[ In\]
</dt> <dd>

Identifiziert den zu aktualisierenden Dienst.

</dd> <dt>

*endpointType* \[ In\]
</dt> <dd>

Identifiziert den Typ des Endpunkts, der zum Herstellen einer Verbindung mit dem Dienst erforderlich ist.

</dd> <dt>

*ulRequestedTypes* \[ In\]
</dt> <dd>

Identifiziert den ORed-Satz von Token, die vom Endpunkt unterstützt werden.

</dd> <dt>

*pulPreferredTokenTypes* \[ out\]
</dt> <dd>

Geben Sie den ORed-Satz von Authentifizierungstokentypen an, die bevorzugt werden. (Legen Sie diesen Wert auf 0 fest, um anzugeben, dass kein Authentifizierungstoken erforderlich ist.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich. Andernfalls wird ein COM- oder Windows zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn diese Methode zurückgegeben wird, wählt WUA einen Tokentyp aus den bevorzugten Typen aus und übergibt ihn an den tokenType-Parameter der [**GetEndpointToken-Methode.**](iupdateendpointauthprovider-getendpointtoken.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




