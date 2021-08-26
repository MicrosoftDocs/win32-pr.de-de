---
description: Der Quellcode für eine benutzerdefinierte Beispielaktion namens Launch, die den Beispielspezifikationen entspricht, wird vom Windows Installer SDK als Datei Tutorial.cpp bereitgestellt.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Erstellen der benutzerdefinierten Aktion "Starten"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536f22c95d871ab502518a0619efad5ae70cb348cdf75163fc50309b440f6393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045272"
---
# <a name="authoring-the-launch-custom-action"></a>Erstellen der benutzerdefinierten Aktion "Starten"

Der Quellcode für eine benutzerdefinierte Beispielaktion namens Launch, die den Beispielspezifikationen entspricht, wird vom Windows Installer SDK als Datei Tutorial.cpp bereitgestellt. Diese benutzerdefinierte Aktion verwendet [**MsiFormatRecord,**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) um eine Zeichenfolge zu formatieren, die Eigenschaften enthält. Die \[ \# FileKey-Eigenschaft \] wird in den vollständigen Pfad der HTML-Datei aufgelöst. Verwenden Sie die Quelldatei, um die Datei Tutorial.dll zu erstellen. Der Einstiegspunkt für diese DLL ist LaunchTutorial.

Die benutzerdefinierte Beispielaktion Launch ruft eine in C++ geschriebene DLL auf und wird aus einem temporären binären Datenstrom generiert. Benutzerdefinierte Aktionen dieses Typs umfassen die Basistypkonstanten msidbCustomActionTypeDll und msidbCustomActionTypeBinaryData, die einen numerischen Basistyp gleich 1 ergeben. Weitere Informationen finden Sie unter [Benutzerdefinierter Aktionstyp 1.](custom-action-type-1.md) Da die Spezifikationen erfordern, dass die Installation fortgesetzt wird, wenn die benutzerdefinierte Aktion fehlschlägt, enthält Launch auch die optionale Konstante **msidbCustomActionTypeContinue**, die 64 ist. Weitere Informationen finden Sie unter [Rückgabeverarbeitungsoptionen für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md) Der gesamte numerische Typ von Launch ist 65.

Fahren Sie mit [dem Hinzufügen von Launch zu den Tabellen CustomAction und Binary](adding-launch-to-the-customaction-and-binary-tables.md)fort.

 

 



