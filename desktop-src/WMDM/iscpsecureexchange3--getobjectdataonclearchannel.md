---
title: Getobjectdataonclearchannel-Methode
description: Die getobjectdataonclearchannel-Methode überträgt einen Block von Objektdaten auf einem unverschlüsselten Kanal zurück an den Windows Media-Device Manager.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Getobjectdataonclearchannel-Methode, Windows Media Device Manager
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364409"
---
# <a name="getobjectdataonclearchannel-method"></a>Getobjectdataonclearchannel-Methode

Die **getobjectdataonclearchannel** -Methode überträgt einen Block von Objektdaten auf einem unverschlüsselten Kanal zurück an den Windows Media-Device Manager.

Diese Methode ist mit [**iscpsecureexchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) identisch, mit dem Unterschied, dass die von dieser Methode zurückgegebenen Daten nicht verschlüsselt werden. Folglich ist diese Methode effizienter.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* 
</dt> <dd>

Zeiger auf das Geräte Objekt.

</dd> <dt>

*pData* 
</dt> <dd>

Zeiger auf einen Puffer zum Empfangen von Daten.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Zeiger auf ein **DWORD** , das die Übertragungs Größe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn die Methode fehlschlägt, wird ein **HRESULT** -Fehlercode zurückgegeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler beim Überprüfen von WMDM \_ E \_ Mac. \_ \_**</dt> </dl> | Der Nachrichten Authentifizierungscode ist ungültig.<br/>                                    |
| <dl> <dt>**WMDM \_ E- \_ norights**</dt> </dl>           | Der Aufrufer verfügt nicht über die erforderlichen Rechte, um den angeforderten Vorgang auszuführen.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Die Methode ist fehlgeschlagen. Beenden Sie die Interaktion mit dem Inhaltsanbieter.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>               | Ein Parameter ist ein ungültiger oder **null** -Zeiger.<br/>                                   |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                     | Es ist ein unbekannter Fehler aufgetreten.<br/>                                                   |



 

## <a name="remarks"></a>Bemerkungen

Zum Übertragen von Daten ruft Windows Media Device Manager die [transfercontainerdataonclearchannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) -Methode auf, um die Containerdaten abzurufen. **Getobjectdataonclearchannel** wird aufgerufen, um Blöcke von Objektdaten vom Inhaltsanbieter an Windows Media Device Manager zu übertragen. Wenn S \_ OK zurückgegeben wird und *pdwSize* auf NULL festgelegt ist, fordert Windows Media Device Manager keine weiteren Daten an.

Diese Methode ist mit [**iscpsecureexchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) identisch, mit dem Unterschied, dass die von dieser Methode zurückgegebenen Daten nicht verschlüsselt werden. Folglich ist diese Methode effizienter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmscp. idl</dt> </dl>    |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscpsecureexchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**ISCPSecureExchange3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





