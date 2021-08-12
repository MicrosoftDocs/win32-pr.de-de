---
description: DIE CABINETDLLVERSIONINFO enthält die Versionsinformationen für Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: CABINETDLLVERSIONINFO-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9276a03d28bdfeee2b97b44e180bf190cbf20fc40ec58d0aafb44962a6e8fa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667983"
---
# <a name="cabinetdllversioninfo-structure"></a>CABINETDLLVERSIONINFO-Struktur

\[Diese Struktur enthält Informationen, die nur erforderlich sind, wenn die **DllGetVersion-Funktion** verwendet wird, die nicht unterstützt wird. Diese Dokumentation dient nur zu Informationszwecken.\]

DIE **CABINETDLLVERSIONINFO enthält** die Versionsinformationen für Cabinet.dll.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**cbStruct**
</dt> <dd>

Die Größe dieser Struktur in Bytes.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reserviert.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reserviert.

</dd> <dt>

**dwFileVersionMS**
</dt> <dd>

Enthält die wichtigsten Bits der Versionsinformationen. Bits 0-15 enthalten die Nebenversion, bits 16-31 die Hauptversion.

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

Enthält die am wenigsten signifikanten Bits der Versionsinformationen. Die Bits 0 bis 15 enthalten die Revisionsnummer, die Bits 16-31 die Buildnummer.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



