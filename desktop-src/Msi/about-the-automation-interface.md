---
description: Zunächst muss ein Installer-Objekt erstellt werden, um die Automatisierungsunterstützung zu laden, die für den Zugriff auf die Installerkomponenten über COM erforderlich ist.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Informationen zur Automation-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51469240ad684d6fd32ffbc5466007e73f4e4ff7a870b6878b18f25f54d32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382067"
---
# <a name="about-the-automation-interface"></a>Informationen zur Automation-Schnittstelle

Zunächst [**muss ein Installer-Objekt**](installer-object.md) erstellt werden, um die Automatisierungsunterstützung zu laden, die für den Zugriff auf die Installerkomponenten über COM erforderlich ist. Dieses Objekt stellt Wrapper zum Erstellen der Objekte der obersten Ebene und zum Zugreifen auf ihre Methoden zur Hand. Diese Wrapper stellen einfach Parameterübersetzungen zur Verfügung, um die Installerfunktionen auf eine Weise verfügbar zu machen, die mit Microsoft Visual Basic, ohne das Verhalten der Methoden zu ändern.

Wenn möglich, wird ein Paar von Get- und Set-C++-Methoden Visual Basic als einzelne Eigenschaft verfügbar gemacht. In einigen Fällen werden C++-Methoden, die ein Indexargument verwenden, als indizierte Eigenschaft verfügbar gemacht. Viele C++-Methoden geben das Ergebnis über einen Parameter zurück, da der Rückgabewert für die Fehler zurückgegeben wird. In der Visual Basic werden Fehler jedoch durch einen separaten Mechanismus behandelt, und das Ergebnis wird immer im Rückgabewert übergeben.

Informationen zur Verwendung der Automatisierung und zum Erstellen des Installer-Objekts finden Sie unter [Verwenden der Automation-Schnittstelle.](using-the-automation-interface.md)

Referenzmaterial für die Objekte des Windows Installers finden Sie unter [Automation Interface Reference (Referenz zur Automation-Schnittstelle).](automation-interface-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



