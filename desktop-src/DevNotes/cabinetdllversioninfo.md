---
description: "\"Cabinetdllversioninfo\" enthält die Versionsinformationen für Cabinet.dll."
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Cabinetdllversioninfo-Struktur
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
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861008"
---
# <a name="cabinetdllversioninfo-structure"></a>Cabinetdllversioninfo-Struktur

\[Diese Struktur enthält Informationen, die nur erforderlich sind, wenn die **dllgetversion** -Funktion verwendet wird, die nicht unterstützt wird. Diese Dokumentation wird nur zu Informationszwecken bereitgestellt.\]

" **Cabinetdllversioninfo** " enthält die Versionsinformationen für Cabinet.dll.

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

Die Größe der-Struktur in Bytes.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reserviert.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reserviert.

</dd> <dt>

**dwfileversionms**
</dt> <dd>

Enthält die wichtigsten Bits der Versionsinformationen. Bits 0-15 enthalten die neben Version, und Bits 16-31 enthalten die Hauptversion.

</dd> <dt>

**dwfileversionls**
</dt> <dd>

Enthält die am wenigsten wichtigen Bits der Versionsinformationen. Bits 0-15 enthalten die Revisionsnummer, und Bits 16-31 enthalten die Buildnummer.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dllgetversion**](dllgetversion.md)
</dt> </dl>

 

 



