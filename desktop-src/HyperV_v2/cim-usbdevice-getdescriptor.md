---
description: Gibt den von den Eingabe Parametern angegebenen "tobdevice"-Deskriptor zurück.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: GetDescriptor-Methode der CIM_USBDevice-Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345887"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>GetDescriptor-Methode der CIM_USBDevice-Klasse (Hyper-V-Verwaltung)

Gibt den von den Eingabe Parametern angegebenen "tobdevice"-Deskriptor zurück.

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

*RequestType* \[ in\]
</dt> <dd>

Bitmap, die den Typ der deskriptoranforderung und den Empfänger angibt. Der Typ der Anforderung kann "Standard", "Class" oder "Vendor-Specific" lauten. Der Empfänger kann "Device", "Interface", "Endpoint" oder "Other" lauten. Die entsprechenden Werte für jedes Bit finden Sie in der USB-Spezifikation.

</dd> <dt>

*Requestvalue* \[ in\]
</dt> <dd>

Enthält den Deskriptortyp im hohen Byte und den deskriptorindex (z. b. Index oder Offset im deskriptorarray) im unteren Byte. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestIndex* \[ in\]
</dt> <dd>

Definiert den 2-Byte-Sprach-ID-Code, der von "rbdevice" beim Zurückgeben von Zeichen folgen deskriptordaten Der-Parameter ist in der Regel 0 für nicht-Zeichen folgen Deskriptoren. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

Enthält bei Eingabe die Länge (in Oktette) des Deskriptors, der zurückgegeben werden soll. Wenn dieser Wert kleiner als die tatsächliche Länge des Deskriptors ist, wird nur die angeforderte Länge zurückgegeben. Wenn Sie größer als die tatsächliche Länge ist, wird die tatsächliche Länge zurückgegeben. Bei der Ausgabe ist dieser Parameter die Länge des zurückgegebenen Puffers in Oktets. Wenn der angeforderte Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.

</dd> <dt>

*Puffer* \[ vorgenommen\]
</dt> <dd>

Gibt die angeforderten Deskriptorinformationen zurück. Wenn der Deskriptor nicht vorhanden ist, ist der Inhalt des Parameters nicht definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM-Start \_ Gerät**](cim-usbdevice.md)
</dt> </dl>

 

 




