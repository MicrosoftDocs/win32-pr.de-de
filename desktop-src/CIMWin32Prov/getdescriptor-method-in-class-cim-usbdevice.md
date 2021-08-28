---
description: Die GetDescriptor-Methode gibt den USB-Gerätedeskriptor zurück, wie von den Eingabeparametern angegeben.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: GetDescriptor-Methode der CIM_USBDevice-Klasse (Wmcodecdsp.h)
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
ms.openlocfilehash: 1288ab1c00ec51c61d3a5e2f7c013ca1e3728fc88087092868421f8e11b7f0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077540"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a>GetDescriptor-Methode der CIM_USBDevice-Klasse (Wmcodecdsp.h)

Die **GetDescriptor-Methode** gibt den USB-Gerätedeskriptor zurück, wie von den Eingabeparametern angegeben.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Bitzuordnungsbezeichner für den Typ der Deskriptoranforderung und des Empfängers. Die entsprechenden Werte für jedes Bit finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestValue* \[ In\]
</dt> <dd>

Enthält den Deskriptortyp im hohen Byte und den Deskriptorindex (z. B. Index oder Offset in das Deskriptorarray) im unteren Byte. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestIndex* \[ In\]
</dt> <dd>

Gibt den 2-Byte-Sprachbezeichnercode an, der vom USB-Gerät beim Zurückgeben von Zeichenfolgendeskriptordaten verwendet wird. Der Parameter ist in der Regel 0 (null) für Nichtzeichenfolgendeskriptoren. Weitere Informationen finden Sie in der USB-Spezifikation.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

Bei der Eingabe die Länge (in Oktetten) des Deskriptors, der zurückgegeben werden soll. Wenn dieser Wert kleiner als die tatsächliche Länge des Deskriptors ist, wird nur die angeforderte Länge zurückgegeben. Wenn sie größer als die tatsächliche Länge ist, wird die tatsächliche Länge zurückgegeben.

Bei der Ausgabe die Länge (in Oktetten) des zurückgegebenen Puffers. Wenn der angeforderte Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.

</dd> <dt>

*Puffer* \[ out\]
</dt> <dd>

Gibt die angeforderten Deskriptorinformationen zurück. Wenn der Deskriptor nicht vorhanden ist, ist der Inhalt dieses Parameters nicht definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der USB-Deskriptor erfolgreich zurückgegeben wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben. In einer Unterklasse kann der Satz möglicher Rückgabecodes  mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. Die Zeichenfolgen, in die der mofqualifier-Inhalt übersetzt wird, können auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. 

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ USBDevice**](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

