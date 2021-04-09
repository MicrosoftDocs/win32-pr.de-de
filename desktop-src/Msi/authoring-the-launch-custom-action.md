---
description: Der Quellcode für eine benutzerdefinierte Beispiel Aktion mit dem Namen "Launch", die den Beispiel Spezifikationen entspricht, wird vom Windows Installer SDK als Datei "Tutorial. cpp" bereitgestellt.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Erstellen der benutzerdefinierten Aktion "starten"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959507"
---
# <a name="authoring-the-launch-custom-action"></a>Erstellen der benutzerdefinierten Aktion "starten"

Der Quellcode für eine benutzerdefinierte Beispiel Aktion mit dem Namen "Launch", die den Beispiel Spezifikationen entspricht, wird vom Windows Installer SDK als Datei "Tutorial. cpp" bereitgestellt. Durch diese benutzerdefinierte Aktion wird [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) verwendet, um eine Zeichenfolge zu formatieren, die Eigenschaften enthält. Die Eigenschaft \[ \# filekey wird \] in den vollständigen Pfad der HTML-Datei aufgelöst. Erstellen Sie die Datei Tutorial.dll mithilfe der Quelldatei. Der Einstiegspunkt für diese dll ist "launchtutorial".

Das Beispiel zum Starten einer benutzerdefinierten Aktion ruft eine in C++ geschriebene dll auf und wird aus einem temporären binären Stream generiert. Benutzerdefinierte Aktionen dieses Typs umfassen die Basistyps msidbcustomaktiontypedll und msidbcustomaktiontypebinarydata, die einen numerischen Basis-Typ gleich 1 angeben. Siehe [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md). Da die Spezifikationen erfordern, dass die Installation fortgesetzt wird, wenn die benutzerdefinierte Aktion fehlschlägt, schließt Launch auch die optionale Konstante **msidbcustomaction typecontinue** ein, die 64 ist. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md). Der gesamte numerische Starttyp ist 65.

Fahren Sie mit [dem Hinzufügen von Start zu den Tabellen CustomAction und Binary](adding-launch-to-the-customaction-and-binary-tables.md)fort.

 

 



