---
title: COM-, DCOM-und Typbibliotheken
description: Component Object Model (com) und verteiltes Component Object Model (DCOM) verwenden Remote Prozedur Aufrufe (RPC), damit verteilte Komponenten Objekte miteinander kommunizieren können.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- Schnittstellen (mittlere Mitte, com)
- Schnittstellen-Mittell, DCOM
- Schnittstellen-Mittell, Typbibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f0b21aad9f88f02d8029d478eead50f5501ecc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858218"
---
# <a name="com-dcom-and-type-libraries"></a>COM-, DCOM-und Typbibliotheken

Component Object Model (com) und verteiltes Component Object Model (DCOM) verwenden Remote Prozedur Aufrufe (RPC), damit verteilte Komponenten Objekte miteinander kommunizieren können. Daher definiert eine com-oder DCOM-Schnittstelle die Identität und die externen Merkmale eines COM-Objekts. Sie bildet die Mittel, mit denen Clients Zugriff auf die Methoden und Daten eines Objekts erhalten können. Mit DCOM ist dieser Zugriff unabhängig davon möglich, ob die Objekte im gleichen Prozess, unterschiedlichen Prozessen auf demselben Computer oder auf unterschiedlichen Computern vorhanden sind. Wie bei RPC-Client-/Serverschnittstellen kann ein com-oder DCOM-Objekt seine Funktionalität auf verschiedene Weise und über mehrere Schnittstellen verfügbar machen.

## <a name="type-library"></a>Typbibliothek

Eine Typbibliothek (. tlb) ist eine Binärdatei, in der Informationen zu den Eigenschaften und Methoden eines com-oder DCOM-Objekts in einem Formular gespeichert werden, das von anderen Anwendungen zur Laufzeit zugänglich ist. Mithilfe einer Typbibliothek kann eine Anwendung oder ein Browser ermitteln, welche Schnittstellen ein Objekt unterstützt, und die Schnittstellen Methoden eines Objekts aufrufen. Dies kann auch vorkommen, wenn die Objekt-und Client Anwendungen in verschiedenen Programmiersprachen geschrieben wurden. Die COM/DCOM-Laufzeitumgebung kann auch eine Typbibliothek verwenden, um automatische, prozessübergreifende, prozessübergreifende und Computer übergreifende Marshalling für Schnittstellen bereitzustellen, die in Typbibliotheken beschrieben werden.

## <a name="characteristics-of-an-interface"></a>Merkmale einer Schnittstelle

Sie definieren die Eigenschaften einer Schnittstelle in einer Schnittstellen Definitionsdatei (IDL) und einer optionalen Anwendungs Konfigurationsdatei (ACF):

-   Die IDL-Datei gibt die Merkmale der Schnittstellen der Anwendung auf dem Netzwerk an – d. h., wie Daten zwischen Client und Server oder zwischen COM-Objekten übertragen werden sollen.
-   Die ACF-Datei gibt Schnittstellen Merkmale an, z. b. Bindungs Handles, die sich nur auf die lokale Betriebsumgebung beziehen. In der ACF-Datei kann auch angegeben werden, wie eine komplexe Datenstruktur in einem Computer unabhängigen Formular gemarshallt und übertragen werden soll.

Weitere Informationen zu IDL-und ACF-Dateien finden Sie in [den IDL-und ACF-Dateien](/windows/desktop/Rpc/the-idl-and-acf-files).

Bei den IDL-und ACF-Dateien handelt es sich um Skripts, die in Microsoft Interface Definition Language (mittlerer l) geschrieben wurden. Dies ist die Microsoft-Implementierung und-Erweiterung der OSF-DCE Interface Definition Language (IDL). Die Microsoft-Erweiterungen für die IDL-Sprache ermöglichen Ihnen das Erstellen von COM-Schnittstellen und Typbibliotheken. Der Compiler (Midl.exe) verwendet diese Skripts zum Generieren von Stub-und Header Dateien der C-Sprache sowie von Typbibliotheks Dateien.

## <a name="the-midl-compiler"></a>Der Mittel l-Compiler

Abhängig vom Inhalt Ihrer IDL-Datei generiert der-compilercompiler eine der folgenden Dateien.

Eine C-sprachige Proxy-/Stubdatei, eine schnittstellenbezeichnerdatei, eine DLL-Datendatei und eine zugehörige Header Datei für eine benutzerdefinierte COM-Schnittstelle. Der mittlerer l-Compiler generiert diese Dateien, wenn er auf das Object-Attribut in einer Schnittstellen Attribut Liste stößt. Ausführlichere Informationen zu diesen Dateien finden Sie unter [Dateien, die für eine COM-Schnittstelle generiert](files-generated-for-a-com-interface.md)wurden.

Eine kompilierte Typbibliotheks Datei (. tlb) und eine zugehörige Header Datei. Diese Dateien werden von der Mittell generiert, wenn Sie in der IDL-Datei auf eine [**Bibliotheks**](library.md) Anweisung trifft. Allgemeine Informationen zu Typbibliotheken finden Sie unter [Inhalt einer Typbibliothek](/previous-versions/windows/desktop/automat/contents-of-a-type-library)in der Automation-Programmier Referenz.

C/C++-Sprachen Client-und Server-Stub-Dateien und zugehörige Header Datei für eine RPC-Schnittstelle. Diese Dateien werden generiert, wenn in der IDL-Datei Schnittstellen vorhanden sind, die nicht über das [**Object**](object.md) -Attribut verfügen. Eine Übersicht über die Stub-und Header Dateien finden Sie unter [Allgemeine buildprozedur](/windows/desktop/Rpc/general-build-procedure). Ausführlichere Informationen finden Sie unter [Dateien, die für eine RPC-Schnittstelle generiert](files-generated-for-an-rpc-interface.md)wurden.

 

 