---
description: Der Wert der Zusammenfassungseigenschaft Revisionsnummer im Zusammenfassungsinformationsstream muss beim Lokalisieren einer Datenbank in einen neuen eindeutigen Wert geändert werden, da die Installationsdatenbank geändert wird. Weitere Informationen finden Sie unter Paketcodes.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Aktualisieren eines Zusammenfassungsinformationsstreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d95e6a0cf09af5d4a024f707c0694d89def47abf8f731f394c55a11232bc07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039280"
---
# <a name="updating-a-summary-information-stream"></a>Aktualisieren eines Zusammenfassungsinformationsstreams

Der Wert der Zusammenfassungseigenschaft [](summary-information-stream.md) [**Revisionsnummer**](revision-number-summary.md) im Zusammenfassungsinformationsstream muss beim Lokalisieren einer Datenbank in einen neuen eindeutigen Wert geändert werden, da die Installationsdatenbank geändert wird. Weitere Informationen [finden Sie unter Paketcodes](package-codes.md).

Der Wert der [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) im Zusammenfassungsinformationsstream muss in den numerischen Sprachbezeichner (LANGID) der neuen Sprache geändert werden.

Wenn die beschreibenden Textzeichenfolgen im Zusammenfassungsinformationsstream in der neuen Sprache lokalisiert werden, muss die [**Codepage Summary-Eigenschaft**](codepage-summary.md) auf die richtige Codepage für die neue Sprache festgelegt werden.

Sie können den Zusammenfassungsinformationsstream des lokalisierten Pakets mit dem gleichen Verfahren wie unter Hinzufügen von [Zusammenfassungsinformationen ändern.](adding-summary-information.md) Ein Beispiel, das die Verwendung der Methoden für Datenbankzusammenfassungsinformationen demonstriert, wird auch im Windows Installer SDK als Hilfsprogramm WiSumInf.vbs. Weitere Informationen zu WiSumInf.vbs finden Sie unter [Verwalten von Zusammenfassungsinformationen.](manage-summary-information.md)

[Fortsetzen](adding-localized-resources.md)

 

 



