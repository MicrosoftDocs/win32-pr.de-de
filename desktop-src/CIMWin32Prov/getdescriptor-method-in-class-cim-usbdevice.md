---
description: Die getDescriptor-Methode gibt den von den Eingabe Parametern angegebenen USB-Gerätedeskriptor zurück.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: GetDescriptor-Methode der CIM_USBDevice-Klasse (wmcodecdsp. h)
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
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344819"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a>GetDescriptor-Methode der CIM_USBDevice-Klasse (wmcodecdsp. h)

Die **getDescriptor** -Methode gibt den von den Eingabe Parametern angegebenen USB-Gerätedeskriptor zurück.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

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

Bit-zugeordneter Bezeichner für den Typ der deskriptoranforderung und den Empfänger. Die entsprechenden Werte für jedes Bit finden Sie in der USB-Spezifikation.

</dd> <dt>

*Requestvalue* \[ in\]
</dt> <dd>

Enthält den Deskriptortyp im hohen Byte und den deskriptorindex (z. b. Index oder Offset im deskriptorarray) im unteren Byte. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestIndex* \[ in\]
</dt> <dd>

Gibt den 2-Byte-sprach bezeichnercode an, der vom USB-Gerät beim Zurückgeben von Zeichen folgen deskriptordaten verwendet wird Der-Parameter ist in der Regel 0 (null) für nicht Zeichen folgen Deskriptoren. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

Bei Eingabe die Länge (in Oktette) des Deskriptors, der zurückgegeben werden soll. Wenn dieser Wert kleiner als die tatsächliche Länge des Deskriptors ist, wird nur die angeforderte Länge zurückgegeben. Wenn Sie größer als die tatsächliche Länge ist, wird die tatsächliche Länge zurückgegeben.

Bei Ausgabe die Länge (in Oktette) des Puffers, der zurückgegeben wird. Wenn der angeforderte Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.

</dd> <dt>

*Puffer* \[ vorgenommen\]
</dt> <dd>

Gibt die angeforderten Deskriptorinformationen zurück. Wenn der Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert von 0 (null) zurück, wenn der USB-Deskriptor erfolgreich zurückgegeben wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an. In einer Unterklasse können die möglichen Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden. Die Zeichen folgen, auf die der Inhalt des "fifqualifizierers" übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zurzeit nicht von WMI implementiert. Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM-Start \_ Gerät**](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[**CIM-Start \_ Gerät**](cim-usbdevice.md)
</dt> </dl>

 

