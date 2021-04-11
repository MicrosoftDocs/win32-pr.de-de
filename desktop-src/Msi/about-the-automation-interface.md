---
description: Ein Installer-Objekt muss anfänglich erstellt werden, um die für den Zugriff auf die Installationsprogramm Komponenten über com erforderliche Automatisierungsunterstützung zu laden.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Informationen zur Automatisierungsschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215732"
---
# <a name="about-the-automation-interface"></a>Informationen zur Automatisierungsschnittstelle

Ein [**Installer-Objekt**](installer-object.md) muss anfänglich erstellt werden, um die für den Zugriff auf die Installationsprogramm Komponenten über com erforderliche Automatisierungsunterstützung zu laden. Dieses Objekt stellt Wrapper zum Erstellen der Objekte der obersten Ebene und zum Zugreifen auf ihre Methoden bereit. Diese Wrapper stellen einfach Parameter Übersetzungen bereit, um die Installer-Funktionen in Übereinstimmung mit Microsoft Visual Basic verfügbar zu machen, ohne das Verhalten der Methoden zu ändern.

Wenn möglich, werden ein paar von Get-und Set C++-Methoden für Visual Basic als einzelne Eigenschaft verfügbar gemacht. In einigen Fällen werden C++-Methoden, die ein Index-Argument übernehmen, als indizierte Eigenschaft verfügbar gemacht. Viele C++-Methoden geben das Ergebnis über einen Parameter zurück, da der Rückgabewert für die Fehlerrückgabe verwendet wird. In Visual Basic werden Fehler jedoch von einem separaten Mechanismus behandelt, und das Ergebnis wird immer im Rückgabewert übermittelt.

Informationen zum Verwenden von Automation und zum Erstellen des Installations Objekts finden Sie unter [Verwenden der Automatisierungsschnittstelle](using-the-automation-interface.md).

Referenzmaterial für die Windows Installer-Objekte finden Sie unter [Automation Interface Reference](automation-interface-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



