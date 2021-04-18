---
title: Verwenden neuer Datentypen in ihrer IDL-Datei
description: Die Header Datei "basetsd. h" definiert die neuen Datentypen, die zum Schreiben von Anwendungen benötigt werden, die sowohl unter 32-als auch 64-Bit-Windows ausgeführt werden.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Basetsd. h-Header Datei 64-Bit-Windows-Programmierung
- Datentypen in der IDL-Datei 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337655"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Verwenden neuer Datentypen in ihrer IDL-Datei

Die Header Datei "basetsd. h" definiert die neuen Datentypen, die zum Schreiben von Anwendungen benötigt werden, die sowohl unter 32-als auch 64-Bit-Windows ausgeführt werden. Um diese Datentypen in ihren Schnittstellen zu verwenden, importieren Sie basetsd. h in Ihre IDL-Datei. \#Schließen Sie die Datei nicht ein, oder es werden mehrere Definitionen zum Zeitpunkt der Kompilierung erstellt.

Alternativ dazu können Sie die Datei "basetsd. idl" in Ihre IDL-Datei einschließen oder importieren.

Weitere Informationen zum Hinzufügen von System Header Dateien zu ihrer IDL-Datei finden Sie unter [Importieren von Dateien und Typbibliotheken](/windows/desktop/Midl/importing-files-and-type-libraries) und [Importieren von System Header Dateien](/windows/desktop/Midl/importing-system-header-files).

 

 