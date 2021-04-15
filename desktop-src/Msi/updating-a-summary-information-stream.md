---
description: Der Wert der Zusammenfassungs Eigenschaft "Revisionsnummer" im Zusammenfassungs Informationsdaten Strom muss bei der Lokalisierung einer Datenbank in einen neuen, eindeutigen Wert geändert werden, da die Installations Datenbank geändert wird. Siehe Paket Codes.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Aktualisieren eines Zusammenfassungs Informationsdaten Stroms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393773"
---
# <a name="updating-a-summary-information-stream"></a>Aktualisieren eines Zusammenfassungs Informationsdaten Stroms

Der Wert der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) muss bei der Lokalisierung einer Datenbank in einen neuen, eindeutigen Wert geändert werden, da die Installations Datenbank geändert wird. Siehe [Paket Codes](package-codes.md).

Der Wert der [**Template Summary**](template-summary.md) -Eigenschaft im Zusammenfassungs Informationsdaten Strom muss in den numerischen sprach Bezeichner (langid) der neuen Sprache geändert werden.

Wenn die beschreibenden Text Zeichenfolgen im Zusammenfassungs Informationsdaten Strom in die neue Sprache lokalisiert werden, muss die [**Codepage-Zusammenfassungs**](codepage-summary.md) Eigenschaft auf die richtige Codepage für die neue Sprache festgelegt werden.

Sie können den Zusammenfassungs Datenstrom des lokalisierten Pakets mit dem gleichen Verfahren wie beim [Hinzufügen von Zusammenfassungs Informationen](adding-summary-information.md)ändern. Ein Beispiel für die Verwendung der Methoden zur Daten Bank Zusammenfassung finden Sie auch im Windows Installer SDK als Dienst WiSumInf.vbs. Weitere Informationen zu WiSumInf.vbs finden Sie unter [Verwalten von Zusammenfassungs Informationen](manage-summary-information.md).

[Fortsetzen](adding-localized-resources.md)

 

 



