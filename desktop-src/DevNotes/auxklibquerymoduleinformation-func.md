---
description: Ruft Informationen über den derzeit geladenen Satz von Modulen für das System ab.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Funktion "AuxKlibQueryModuleInformation" \_ (Aux-Funktion "Aux"-Datei ".h"))
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
ms.openlocfilehash: be734583c8b7d02be4c498bc75069a0c813565d48aea3db3826712d6375e72b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045315"
---
# <a name="auxklibquerymoduleinformation-function"></a>AuxKlibQueryModuleInformation-Funktion

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

Bei der Eingabe die Größe des *QueryInfo-Puffers* in Bytes. Empfängt bei der Ausgabe die tatsächlich erforderliche Größe. Da sich die Liste der Systemmodule zwischen Aufrufen ändern kann, kann sich dieser Wert auch zwischen Aufrufen ändern.

</dd> <dt>

*ElementSize* \[ In\]
</dt> <dd>

Die Größe eines Arrayelements in Bytes. Diese Größe bestimmt das Format der Ausgabe.

</dd> <dt>

*QueryInfo* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Modulinformationen empfängt. Diese Informationen werden in einem Array zurückgegeben, dessen Elemente eine der folgenden Strukturen sind: [**AUX \_ MODULE BASIC \_ \_ INFO**](aux-module-basic-info-struct.md) oder [**AUX MODULE EXTENDED \_ \_ \_ INFO**](aux-module-extended-info-struct.md). Die verwendete spezifische Struktur hängt von der angegebenen Elementgröße ab.

Wenn dieser Parameter **NULL ist,** gibt die Funktion die erforderliche Puffergröße zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert STATUS \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der status-Codes sein, die in Ntstatus.h definiert sind, der im WDK verfügbar ist.

## <a name="remarks"></a>Hinweise

Sie müssen die [**AuxKlibInitialize-Funktion aufrufen,**](auxklibinitialize-func.md) bevor Sie diese Funktion aufrufen.

Die Objektbibliothek, die diese API implementiert, kann hier heruntergeladen [werden.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|------------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Zusätzliche API-Bibliothek, Version 1.0 oder höher<br/>                            |
| Header<br/>          | <dl> <dt>\_Aux-Datei ".h"</dt> </dl>   |
| Bibliothek<br/>         | <dl> <dt>\_Aux-Datei "Aux"-Datei ".lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**GRUNDLEGENDE INFORMATIONEN \_ ZUM AUX-MODUL \_ \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**ERWEITERTE INFORMATIONEN \_ ZUM AUX-MODUL \_ \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




