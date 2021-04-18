---
description: Gibt den bevorzugten Authentifizierungstyp für den Endpunkt des Diensts zurück.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Iupdateendpointauthprovider:: getpreferredendpointdekentype-Methode (updateendpointauth. h)'
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
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214733"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>Iupdateendpointauthprovider:: getpreferredendpointdekentype-Methode

Gibt den bevorzugten Authentifizierungstyp für den Endpunkt des Diensts zurück.

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

*serviceid* \[ in\]
</dt> <dd>

Identifiziert den zu aktualisierenden Dienst.

</dd> <dt>

*EndpointType* \[ in\]
</dt> <dd>

Identifiziert den Typ des Endpunkts, der zum Herstellen einer Verbindung mit dem Dienst erforderlich ist.

</dd> <dt>

*ulrequestedtypes* \[ in\]
</dt> <dd>

Identifiziert den ORed-Satz von Token, die vom Endpunkt unterstützt werden.

</dd> <dt>

*pulpreferredykentypes* \[ vorgenommen\]
</dt> <dd>

Geben Sie den bevorzugten Satz an authentifizierungstokentypen an. (Auf 0 festgelegt, um anzugeben, dass kein Authentifizierungs Token erforderlich ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode zurückgegeben wird, wählt WUA einen Tokentyp aus den bevorzugten Typen aus und übergibt ihn an den TokenType-Parameter der [**getendpointtoken**](iupdateendpointauthprovider-getendpointtoken.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Updateendpointauth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iupdateendpointauthprovider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**Getendpointtoken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




