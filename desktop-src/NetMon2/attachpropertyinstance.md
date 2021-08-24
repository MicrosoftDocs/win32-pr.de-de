---
description: Die AttachPropertyInstance-Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: AttachPropertyInstance-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c4d726b7500fd890dfe8c7fdc39f628c185dbe35f3a3bc14f0c05ab7f85cd673
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744680"
---
# <a name="attachpropertyinstance-function"></a>AttachPropertyInstance-Funktion

Die **AttachPropertyInstance-Funktion** ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame, der analysiert wird. Verwenden Sie das handle, das an die Parser-DLL im *hFrame-Parameter* der [**AttachProperties-Funktion übergeben**](attachproperties.md) wird.

</dd> <dt>

*hProperty* \[ In\]
</dt> <dd>

Handle für eine [**PROPERTYINFO-Struktur,**](propertyinfo.md) die die -Eigenschaft definiert. Wenn Sie die [**Exportfunktion Register**](register-parser.md) implementieren, geben Sie die **PROPERTYINFO-Struktur** an, die die Eigenschaft definiert.

</dd> <dt>

*Länge* \[ In\]
</dt> <dd>

Länge der Daten für diese Instanz der -Eigenschaft.

</dd> <dt>

*lpData* \[ In\]
</dt> <dd>

Zeiger auf die Position in den erkannten Daten, an der sich der Eigenschaftswert befindet. Verwenden Sie den Zeiger, der an die Parser-DLL im *lpProtocol-Parameter* der [**AttachProperties-Funktion übergeben**](attachproperties.md) wird.

</dd> <dt>

*HelpID* \[ In\]
</dt> <dd>

Bezeichner (von 0 bis 2047), der zum Festlegen der kontextsensitiven Hilfe für die Eigenschaft verwendet wird.

Die Bezeichnernummer ist relativ zur Hilfedatei, die der Protokolleigenschaftsdatenbank [*zugeordnet ist.*](p.md)

</dd> <dt>

*IndentLevel* \[ In\]
</dt> <dd>

Einzugsebene (von 0 bis 15), die verwendet wird, um eine Eigenschaft hierarchisch anzuzeigen.

Netzwerkmonitor verwendet die Ebenen 0 bis 14, um Eigenschaften eingerückt zu werden. Ebene 15 ist ein spezieller Wert, mit dem ein Parser eine ausgeblendete Eigenschaft anfügen kann, die nicht sichtbar ist.

</dd> <dt>

*IFlags* \[ In\]
</dt> <dd>

Ein BIT-Feldwert, der die Reihenfolge der BITs innerhalb einer Eigenschaft angibt. Vorherige Parser, die *fError* auf 0 oder 1 festlegen, sollten *fError* jetzt auf IFLAG \_ ERROR festlegen. Legen Sie diesen Parameter auf einen der folgenden Werte fest.



| Wert                                                                                                                                                         | Bedeutung                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**\_IFLAG-FEHLER**</dt> </dl>       | Daten im Frame haben einen Fehler.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ SWAPPED**</dt> </dl> | Zum Zeitpunkt des Anfügens ist **das WORD-Byte** ein Nicht-Intel-Format.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | Zum Zeitpunkt der Anfügen **ist STRING** Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Die **AttachPropertyInstance-Funktion** wird während der Implementierung der [**AttachProperties-Exportfunktion**](attachproperties.md) aufgerufen. Wenn eine Eigenschaft an die Daten angefügt wird, erstellt Netzwerkmonitor [**PROPERTYINST-Struktur,**](propertyinst.md) die die Instanz der angefügten Eigenschaft definiert.

Rufen Sie während der Implementierung von [**AttachProperties**](attachproperties.md) **AttachPropertyInstance** auf, um die Daten so zu verwenden, wie sie in der Erfassung vorhanden sind. Sie können auch die [**AttachPropertyInstanceEx-Funktion**](attachpropertyinstanceex.md) aufrufen, um die Eigenschaftsdaten zu ändern. Es wird jedoch empfohlen, die Daten so zu verwenden, wie sie in der Erfassung vorhanden sind.



| Informationen zu                                        | Siehe                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor. | [**Parser**](parsers.md)                                         |
| Aufrufen von **AttachPropertyInstance**.                   | [Implementieren von AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AttachProperties**](attachproperties.md)
</dt> <dt>

[**AttachPropertyInstanceEx**](attachpropertyinstanceex.md)
</dt> <dt>

[**PROPERTYINST**](propertyinst.md)
</dt> </dl>

 

 




