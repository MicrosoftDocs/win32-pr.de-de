---
description: Die AttachPropertyInstanceEx-Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu und ändert den Wert der Eigenschaftsdaten.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: AttachPropertyInstanceEx-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ec0b874d55d149c9d049b8c6b2cafd716fe82c66410e2d3e1550b397c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911280"
---
# <a name="attachpropertyinstanceex-function"></a>AttachPropertyInstanceEx-Funktion

Die **AttachPropertyInstanceEx-Funktion** ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu und ändert den Wert der Eigenschaftsdaten.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame, der analysiert wird. Verwenden Sie das Handle, das an die Parser-DLL im *hFrame-Parameter* der [**AttachProperties-Funktion**](attachproperties.md) übergeben wird.

</dd> <dt>

*hProperty* \[ In\]
</dt> <dd>

Handle für eine [**PROPERTYINFO-Struktur,**](propertyinfo.md) die die Eigenschaft definiert. Wenn Sie die [**Exportfunktion Register**](register-parser.md) implementieren, geben Sie die **PROPERTYINFO-Struktur** an, die die Eigenschaft definiert.

</dd> <dt>

*Länge* \[ In\]
</dt> <dd>

Länge der Daten für diese Instanz der -Eigenschaft.

</dd> <dt>

*lpData* \[ In\]
</dt> <dd>

Zeiger auf die Position in den erkannten Daten, an der sich der Eigenschaftswert befindet. Verwenden Sie den Zeiger, der an die Parser-DLL im *lpProtocol-Parameter* der [**AttachProperties-Funktion**](attachproperties.md) übergeben wird.

</dd> <dt>

*LengthEx* \[ In\]
</dt> <dd>

Länge der erweiterten Datenlänge in Bytes.

</dd> <dt>

*lpDataEx* \[ In\]
</dt> <dd>

Zeiger auf die erweiterten Daten, bei denen es sich in der Regel um eine Stapelvariable handelt, die die Extend-Daten enthält.

</dd> <dt>

*HelpID* \[ In\]
</dt> <dd>

Bezeichner (von 0 bis 2047), der verwendet wird, um kontextbezogene Hilfe für eine Eigenschaft festzulegen.

Die *HelpID-Nummer* ist relativ zur Hilfedatei, die der [*Protokolleigenschaftsdatenbank*](p.md)zugeordnet ist.

</dd> <dt>

*IndentLevel* \[ In\]
</dt> <dd>

Einzugsebene (von 0 bis 15), die verwendet wird, um eine Eigenschaft hierarchisch anzuzeigen.

Netzwerkmonitor verwendet die Ebenen 0 bis 9. Ebene 15 ist ein spezieller Wert, mit dem der Parser eine ausgeblendete Eigenschaft anfügen kann, die nicht sichtbar ist.

</dd> <dt>

*IFlags* \[ In\]
</dt> <dd>

Ein BIT-Feldwert, der die Reihenfolge der BITs innerhalb einer Eigenschaft angibt. Vorherige Parser, die *fError* auf 0 oder 1 festgelegt haben, sollten jetzt *fError* auf IFLAG \_ ERROR festlegen. Legen Sie diesen Parameter auf einen der folgenden Werte fest.



| Wert                                                                                                                                                         | Bedeutung                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**\_IFLAG-FEHLER**</dt> </dl>       | Daten im Frame haben einen Fehler.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ GETAUSCHT**</dt> </dl> | Zum Zeitpunkt der Anfügezeit ist **das WORD-Byte** ein Nicht-Intel-Format.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | Beim Anfügen ist **STRING** Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Die **AttachPropertyInstanceEx-Funktion** wird während der Implementierung der [**AttachProperties-Exportfunktion**](attachproperties.md) aufgerufen. Wenn eine Eigenschaft mit AttachPropertyInstanceEx an die Daten angefügt wird, erstellt Netzwerkmonitor eine [**PROPERTYINST-Struktur,**](propertyinst.md) die die Instanz der angefügten Eigenschaft definiert, und eine [**PROPERTYINSTEX-Struktur,**](propertyinstex.md) die die erweiterten Daten definiert.

Wenn **AttachPropertyInstanceEx** aufgerufen wird und keine erweiterten Daten bereitgestellt werden, der *lpDataEx-Parameter* **NULL** oder der *LengthEx-Parameter* 0 ist, entspricht der **AttachPropertyInstanceEx-Aufruf** funktional einem [**AttachPropertyInstance-Aufruf.**](attachpropertyinstance.md)

Rufen Sie während der Implementierung von [**AttachProperties**](attachproperties.md) [**AttachPropertyInstance**](attachpropertyinstance.md) auf, um die Daten so zu verwenden, wie sie in der Erfassung vorhanden sind. Sie können auch **die AttachPropertyInstanceEx-Funktion** aufrufen, um die Eigenschaftsdaten zu ändern. Es wird jedoch empfohlen, die Daten so zu verwenden, wie sie in der Erfassung vorhanden sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




