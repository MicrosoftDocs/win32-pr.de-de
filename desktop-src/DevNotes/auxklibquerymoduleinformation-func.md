---
description: Ruft Informationen über den derzeit geladenen Satz von Modulen für das System ab.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: "\"Auxklibquerymoduleinformation\"-Funktion (AUX \\_ KLIB. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357969"
---
# <a name="auxklibquerymoduleinformation-function"></a>"Auxklibquerymoduleinformation"-Funktion

Ruft Informationen über den derzeit geladenen Satz von Modulen für das System ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BufferSize* \[ in, out\]
</dt> <dd>

Bei Eingabe die Größe des *QueryInfo* -Puffers in Bytes. Bei Ausgabe wird die tatsächlich erforderliche Größe empfangen. Da die Liste der Systemmodule zwischen Aufrufen geändert werden kann, kann dieser Wert auch zwischen Aufrufen geändert werden.

</dd> <dt>

*Element Size* \[ in\]
</dt> <dd>

Die Größe eines Array Elements in Byte. Diese Größe bestimmt das Format der Ausgabe.

</dd> <dt>

*QueryInfo* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Modul Informationen empfängt. Diese Informationen werden in einem Array zurückgegeben, dessen Elemente eine der folgenden Strukturen sind: [**aux \_ Module \_ Basic \_ Info**](aux-module-basic-info-struct.md) oder [**\_ \_ Erweiterte \_ Informationen des aux-Moduls**](aux-module-extended-info-struct.md). Die jeweilige verwendete-Struktur hängt von der angegebenen Elementgröße ab.

Wenn dieser Parameter **null** ist, gibt die Funktion die erforderliche Puffergröße zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der in "NTSTATUS. h" definierten Statuscodes sein, die im WDK verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Sie müssen die Funktion " [**auxklibinitialize**](auxklibinitialize-func.md) " aufrufen, bevor Sie diese Funktion aufrufen.

Die Objektbibliothek, die diese API implementiert, kann [hier](https://www.microsoft.com/?ref=go)heruntergeladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|------------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-Erweiterungs-API-Bibliothek, Version 1,0 oder höher<br/>                            |
| Header<br/>          | <dl> <dt>AUX \_ KLIB. h</dt> </dl>   |
| Bibliothek<br/>         | <dl> <dt>AUX \_ KLIB. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Auxklibinitialize"**](auxklibinitialize-func.md)
</dt> <dt>

[**\_ \_ grundlegende \_ Informationen zu aux-Modulen**](aux-module-basic-info-struct.md)
</dt> <dt>

[**\_ \_ Erweiterte \_ Informationen des aux-Moduls**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




