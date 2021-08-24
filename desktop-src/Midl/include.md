---
title: include-Attribut
description: Die Include-Anweisung von ACF gibt eine oder mehrere Headerdateien an, die in den generierten Stubcode eingeschlossen werden sollen.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- Includeattribut MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ec8deec34a42d39fc3973dff73e9912ecb96bfee62e348ef7aebfee6ee9f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067204"
---
# <a name="include-attribute"></a>include-Attribut

Die **Include-Anweisung von** ACF gibt eine oder mehrere Headerdateien an, die in den generierten Stubcode eingeschlossen werden sollen.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateinamen* 
</dt> <dd>

Gibt den Namen einer oder mehrere C-Sprachheaderdateien an. Verwenden Sie den vollständigen Dateinamen, einschließlich . H-Erweiterung, und schließen Sie jeden Dateinamen in Anführungszeichen ein. Trennen Sie mehrere Headerdateinamen in C-Sprache durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Als Ergebnis der **include-Anweisung** enthält der generierte Stubcode eine Include-Anweisung des C-Präprozessors. **\#** Sie geben die C-Sprachheaderdatei beim Kompilieren der Stubs an. Include-Anweisungen basieren auf dem C-Compilermechanismus zum Durchsuchen der Verzeichnisstruktur nach eingeschlossenen Dateien.

> [!Note]  
> Verwenden Sie [**die import-Direktive**](import.md) anstelle der **include-Direktive** für Systemdateien, die Datentypen enthalten, die Sie der IDL-Datei zur Verfügung stellen möchten. Die  import-Direktive ignoriert Funktionsprototypen und ermöglicht ihnen die Verwendung von MIDL-Compilerschaltern, die die Generierung von Unterstützungsroutinen optimieren.

 

## <a name="examples"></a>Beispiele

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**import**](import.md)
</dt> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> </dl>

 

 




