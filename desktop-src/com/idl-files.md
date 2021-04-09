---
title: IDL-Dateien
description: IDL-Dateien
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858498"
---
# <a name="idl-files"></a>IDL-Dateien

Com verwendet die Microsoft Interface Definition Language (mittlere), um COM-Objekte zu beschreiben. "Mittel l" ist eine Erweiterung der IDL für verteilte Computerumgebungen, die von der Open Software Foundation definiert wurden, die zum Definieren von Schnittstellen für Remote Prozedur Aufrufe in herkömmlichen Client-/Server-Anwendungen entwickelt wurde. Die Mittel l enthält die meisten Attribute und Anweisungen der Object Definition Language (ODL), der ursprünglich zum Generieren von Typbibliotheken für OLE-Automatisierung verwendeten Sprache.

In C++ und Java erstellt ein Entwickler, der ein COM-Objekt erstellt, eine IDL-Datei, die vom-compilercompiler verarbeitet wird, um eine Typbibliothek oder Header-und Proxy Dateien zu erstellen, oder beides. Eine *Typbibliothek* ist eine Binärdatei, die das COM-Objekt oder die COM-Schnittstellen beschreibt. Eine Typbibliothek ist die kompilierte Version der IDL-Datei. Typbibliotheken unterstützen jedoch nur ODL-Semantik. Vor allem können Sie nicht alle Informationen aus einer IDL-Datei darstellen, die sich auf IDL-Attribute wie " \[ [**\_ size**](/windows/desktop/Midl/size-is)" bezieht \] . Sie müssen Proxy Dateien für IDL-Dateien erstellen und verwenden, die von Informations Verlusten in der Typbibliothek betroffen sind.

In Visual Basic erstellt ein Entwickler, der ein COM-Objekt erstellt, keine IDL-Datei. Stattdessen sammelt Visual Basic Informationen mithilfe von Klassen-und Projekteigenschaften und erstellt die Typbibliothek direkt.

 

 