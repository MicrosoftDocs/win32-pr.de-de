---
title: Verwenden neuer Datentypen in Ihrer IDL-Datei
description: Die Headerdatei Basetsd.h definiert die neuen Datentypen, die zum Schreiben von Anwendungen erforderlich sind, die sowohl auf 32- als auch auf 64-Bit-Windows ausgeführt werden.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Basetsd.h-Headerdatei 64-Bit-Windows-Programmierung
- Datentypen in der 64-Bit-Windows-Programmierung der IDL-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccb29ee654dc2ecc1459a4a3e8ba549e8f78a8af26a305725dbce90f469881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993920"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Verwenden neuer Datentypen in Ihrer IDL-Datei

Die Headerdatei Basetsd.h definiert die neuen Datentypen, die zum Schreiben von Anwendungen erforderlich sind, die sowohl auf 32- als auch auf 64-Bit-Windows ausgeführt werden. Um diese Datentypen in Ihren Schnittstellen zu verwenden, importieren Sie Basetsd.h in Ihre IDL-Datei. Schließen Sie die Datei nicht ein, oder Sie erhalten zur \# Kompilierzeit mehrere Definitionen.

Alternativ können Sie die Datei Basetsd.idl in Ihre IDL-Datei einschließen oder importieren.

Weitere Informationen zum Hinzufügen von Systemheaderdateien zu Ihrer IDL-Datei finden Sie unter [Importieren von Dateien und Typbibliotheken und](/windows/desktop/Midl/importing-files-and-type-libraries) Importieren von [Systemheaderdateien.](/windows/desktop/Midl/importing-system-header-files)

 

 