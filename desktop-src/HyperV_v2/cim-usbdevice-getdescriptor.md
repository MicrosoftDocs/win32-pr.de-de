---
description: Gibt den USBDevice-Deskriptor zurück, wie durch die Eingabeparameter angegeben.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: GetDescriptor-Methode der CIM_USBDevice -Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0523cc88205792f9429eb1a214d8b74a1ca4c2f2bf35813c25614f9f3c06199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980780"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>GetDescriptor-Methode der CIM_USBDevice -Klasse (Hyper-V-Verwaltung)

Gibt den USBDevice-Deskriptor zurück, wie durch die Eingabeparameter angegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RequestType* \[ In\]
</dt> <dd>

Bitzuordnung, die den Typ der Deskriptoranforderung und den Empfänger identifiziert. Der Anforderungstyp kann "standard", "class" oder "vendor-specific" sein. Der Empfänger kann "device", "interface", "endpoint" oder "other" sein. Die entsprechenden Werte für jedes Bit finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestValue* \[ In\]
</dt> <dd>

Enthält den Deskriptortyp im hohen Byte und den Deskriptorindex (z. B. Index oder Offset im Descriptorarray) im niedrigen Byte. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestIndex* \[ In\]
</dt> <dd>

Definiert den 2-Byte-Sprach-ID-Code, der von USBDevice verwendet wird, wenn Zeichenfolgendeskriptordaten zurückgegeben werden. Der -Parameter ist in der Regel 0 für Nicht-Zeichenfolgendeskriptoren. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

Enthält bei der Eingabe die Länge (in Oktetten) des Deskriptors, der zurückgegeben werden soll. Wenn dieser Wert kleiner als die tatsächliche Länge des Deskriptors ist, wird nur die angeforderte Länge zurückgegeben. Wenn er größer als die tatsächliche Länge ist, wird die tatsächliche Länge zurückgegeben. Bei der Ausgabe ist dieser Parameter die Länge des zurückgegebenen Puffers in Oktetten. Wenn der angeforderte Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.

</dd> <dt>

*Puffer* \[ out\]
</dt> <dd>

Gibt die angeforderten Deskriptorinformationen zurück. Wenn der Deskriptor nicht vorhanden ist, ist der Inhalt des Parameters nicht definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

 




