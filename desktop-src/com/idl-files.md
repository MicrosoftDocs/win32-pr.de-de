---
title: IDL-Dateien
description: IDL-Dateien
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e2329d14ea844658bf9ad08927ddcef5067debed7a1c8a424c06d3c7adb8d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992900"
---
# <a name="idl-files"></a>IDL-Dateien

COM verwendet die Microsoft Interface Definition Language (MIDL), um COM-Objekte zu beschreiben. MIDL ist eine Erweiterung der IDL für verteilte Computingumgebungen, die von der Open Software Foundation definiert wurden und entwickelt wurde, um Schnittstellen für Remoteprozeduraufrufe in herkömmlichen Client-/Serveranwendungen zu definieren. MIDL enthält die meisten Attribute und Anweisungen der Object Definition Language (ODL), der Sprache, die ursprünglich zum Generieren von Typbibliotheken für OLE-Automatisierung verwendet wurde.

In C++ und Java erstellt ein Entwickler, der ein COM-Objekt erstellt, eine IDL-Datei, die der MIDL-Compiler dann verarbeitet, um eine Typbibliothek oder Header- und Proxydateien oder beides zu erstellen. Eine *Typbibliothek* ist eine Binärdatei, die das COM-Objekt, com-Schnittstellen oder beides beschreibt. Eine Typbibliothek ist die kompilierte Version der IDL-Datei. Typbibliotheken unterstützen jedoch nur ODL-Semantik. Insbesondere können sie nicht alle Informationen aus einer IDL-Datei darstellen, die sich auf IDL-Attribute beziehen, z.B. \[ [**size \_ ist**](/windows/desktop/Midl/size-is) \] . Sie müssen Proxydateien für IDL-Dateien erstellen und verwenden, die von Informationsverlusten in der Typbibliothek betroffen sind.

In Visual Basic erstellt ein Entwickler, der ein COM-Objekt erstellt, keine IDL-Datei. Stattdessen sammelt Visual Basic Informationen mithilfe von Klassen- und Projekteigenschaften und erstellt die Typbibliothek direkt.

 

 