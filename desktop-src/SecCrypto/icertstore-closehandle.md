---
description: Schließt ein HCERTSTORE-handle, das über die StoreHandle-Eigenschaft abgerufen wurde.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Icertstore:: CloseHandle-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361080"
---
# <a name="icertstoreclosehandle-method"></a>Icertstore:: CloseHandle-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **CloseHandle** -Methode schließt ein HCERTSTORE-handle, das über die [**storeHandle**](icertstore-storehandle.md) -Eigenschaft abgerufen wurde.

## <a name="syntax"></a>Syntax


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HCERTSTORE* \[ in\]
</dt> <dd>

Das zu schließende HCERTSTORE-handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert **S \_ OK** weist auf Erfolg hin. Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird das in einem [**Speicher**](store.md) Objekt enthaltene HCERTSTORE-Handle nicht freigegeben. Es sollte nur verwendet werden, um ein HCERTSTORE-Handle freizugeben, das über die [**storeHandle**](icertstore-storehandle.md) -Eigenschaft abgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icertstore**](icertstore.md)
</dt> </dl>

 

 




