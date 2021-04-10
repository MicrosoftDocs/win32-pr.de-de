---
title: include-Attribut
description: Die ACF include-Anweisung gibt eine oder mehrere Header Dateien an, die in den generierten Stub-Code eingeschlossen werden sollen.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- Include-Attribut-Mittel l
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100874"
---
# <a name="include-attribute"></a>include-Attribut

Die ACF **include** -Anweisung gibt eine oder mehrere Header Dateien an, die in den generierten Stub-Code eingeschlossen werden sollen.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateinamen* 
</dt> <dd>

Gibt den Namen einer oder mehrerer C-sprach Header Dateien an. Verwenden Sie den vollständigen Dateinamen, einschließlich der. H-Erweiterung und schließen Sie jeden Dateinamen in Anführungszeichen ein. Trennen Sie mehrere Header Dateinamen der C-Sprache durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Als Ergebnis der **include** -Anweisung enthält der generierte Stub-Code eine **\# include** -Anweisung im C-Präprozessor. Sie stellen die Header Datei der C-Sprache bereit, wenn Sie die Stub kompilieren. Include-Anweisungen basieren auf dem C-compilermechanismus, der die Verzeichnisstruktur für enthaltene Dateien durchsucht.

> [!Note]  
> Verwenden Sie die [**Import**](import.md) -Direktive anstelle der **include** -Direktive für Systemdateien, die Datentypen enthalten, die Sie der IDL-Datei zur Verfügung stellen möchten. Die **Import** -Direktive ignoriert Funktionsprototypen und ermöglicht Ihnen die Verwendung von Mittell-Compilerschaltern, die die Generierung von Unterstützungs Routinen optimieren.

 

## <a name="examples"></a>Beispiele

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Importieren**](import.md)
</dt> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> </dl>

 

 




