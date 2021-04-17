---
title: Imsrdpclientnonscriptable SendKeys-Methode
description: Sendet eine Reihe von Tastatureingaben an das-Steuerelement. Die Tastatureingaben befinden sich in einem Scan-codeformular, bei dem es sich um die Tastatur Daten aus den eigentlichen physischen Schlüsseln handelt.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys-Methode Remotedesktopdienste
- SendKeys-Methode Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste, SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, SendKeys-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477766"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>Imsrdpclientnonscriptable:: SendKeys-Methode

Sendet eine Reihe von Tastatureingaben an das-Steuerelement. Die Tastatureingaben befinden sich in einem Scan-codeformular, bei dem es sich um die Tastatur Daten aus den eigentlichen physischen Schlüsseln handelt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*numKeys* \[ in\]
</dt> <dd>

Die Anzahl der zu sendenden Tastatureingaben. Die maximale Anzahl von Schlüsseln, die in einem Vorgang gesendet werden können, beträgt 20. Die Methode gibt **E \_ invalidArg** zurück, wenn dieser Parameter größer als 20 ist. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> <dt>

*pbarraykeyup* \[ in\]
</dt> <dd>

Ein Array, dessen Größe gleich *numKeys* ist. Ein Element ist " **true** ", wenn der entsprechende Schlüssel auf dem neuesten Stand ist, und " **false** ", wenn der entsprechende Schlüssel nicht

</dd> <dt>

*plkeydata* \[ in\]
</dt> <dd>

Ein Array, dessen Größe gleich *numKeys* ist. Das Array enthält Tastatureingabe-Daten und entspricht dem Wert des *LPARAM* -Parameters der [WM- \_ KeyDown](../inputdev/wm-keydown.md) -Nachricht. Die Daten geben die Wiederholungs Anzahl, den Überprüfungs Code, das erweiterte schlüsselflag, den Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand an. Eine Beschreibung der Bits in diesem Array finden [Sie unter WM- \_ KeyDown](../inputdev/wm-keydown.md).

Das entsprechende Element in *pbarraykeyup* gibt an, ob der Schlüssel nach oben oder unten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Die **SendKeys** -Methode vermischt keine Tastatureingaben, die vom lokalen Benutzer mit Tastatureingaben durchgeführt werden, die von der Methode gesendet werden. Alle an die-Methode weiter gegebenen Tastatureingaben werden in einer einzelnen atomarischen Sequenz an die Remote Sitzung gesendet.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                               |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ imsrdpclientnonscriptable ist als 2f079c4c-87b2-4afd-97ab-20cdb43038ae definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[WM- \_ KeyDown](../inputdev/wm-keydown.md)
</dt> </dl>

 

