---
description: Gibt einen Befehl für ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 aus.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2::D evicecommand-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344456"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2::D evicecommand-Methode

Gibt einen Befehl für ein Windows-Abbild Erfassungs-Hardware Gerät (WIA) 2,0 aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pcmdguid* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Gibt den Befehl an, der an das WIA 2,0-Gerät gesendet werden soll. Weitere Informationen finden Sie unter [_ *WIA-Geräte Befehle* *](-wia-wia-device-commands.md).

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf das [**IWiaItem2**](-wia-iwiaitem2.md) Element, das vom Befehl erstellt wurde (sofern vorhanden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Zusätzlich zu den Standard-COM-Fehlercodes kann die-Methode den folgenden Wert zurückgeben.



| Rückgabecode                                                                                       | Beschreibung                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ cmdnotsupported**</dt> </dl> | Der-Befehl ist nicht für die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle implementiert, für die die-Methode aufgerufen wird. Der numerische Wert für diesen Fehler ist noch nicht definiert. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Verhalten dieser Methode hängt von der Kategorie des Knotens ab, auf dem die Methode aufgerufen wird.

Wenn die Anwendung mithilfe der **IWiaItem2::D evicecommand** -Methode den Befehl [**Bild von WIA \_ cmd über \_ nehmen \_**](-wia-wia-device-commands.md) an das Gerät sendet, erstellt das WIA 2,0-Laufzeitsystem ein [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt, das das Bild darstellt. Die **IWiaItem2::D evicecommand** -Methode speichert die Adresse der Schnittstelle im *ppIWiaItem2* -Parameter.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIWiaItem2* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
