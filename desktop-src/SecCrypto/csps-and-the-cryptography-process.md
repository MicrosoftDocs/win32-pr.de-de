---
description: CryptoAPI-Funktionen verwenden Kryptografiedienstanbieter (CSPs) zum Durchführen von Verschlüsselung und Entschlüsselung sowie zur Bereitstellung von Schlüssel Speicherung und-Sicherheit.
ms.assetid: 7977e59b-7ce1-4bb4-aae4-d67b7d646493
title: CSPs und der kryptografieprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5404fc3641a9a2c753158f5acb84850f3f0f29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041668"
---
# <a name="csps-and-the-cryptography-process"></a>CSPs und der kryptografieprozess

[*CryptoAPI*](../secgloss/c-gly.md) -Funktionen verwenden [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSPs) zum Durchführen von Verschlüsselung und Entschlüsselung sowie zur Bereitstellung von Schlüssel Speicherung und-Sicherheit. Diese CSPs sind unabhängige Module. Idealerweise sind CSPs so geschrieben, dass Sie unabhängig von einer bestimmten Anwendung sind, sodass jede Anwendung mit einer Vielzahl von CSPs ausgeführt werden kann. Tatsächlich haben einige Anwendungen jedoch bestimmte Anforderungen, die einen angepassten CSP erfordern. Dies vergleicht mit dem Windows- [*GDI*](../secgloss/g-gly.md) -Modell. CSPs sind vergleichbar mit grafikgerätetreibern.

Die Qualität des Schutzes für Schlüssel innerhalb des Systems ist ein Entwurfsparameter des CSP und nicht des Systems als Ganzes. Dadurch kann eine Anwendung ohne Änderungen in einer Vielzahl von Sicherheits Kontexten ausgeführt werden.

Die Zugriffs Anwendungen auf die kryptografischen internale sind sorgfältig eingeschränkt. Dadurch wird eine sichere und tragbare Anwendungsentwicklung ermöglicht.

Die folgenden drei Entwurfs Regeln gelten:

-   Anwendungen können nicht direkt auf das Schlüssel Zugriffs Material zugreifen. Da das gesamte Schlüsselmaterial innerhalb des CSP generiert und von der Anwendung durch nicht transparente Handles verwendet wird, besteht kein Risiko, dass eine Anwendung oder die zugehörigen DLLs entweder das Schlüsselmaterial auswählt oder Material aus schlechten Zufalls Quellen auswählt.
-   Anwendungen können die Details von kryptografievorgängen nicht angeben. Die CSP-Schnittstelle ermöglicht einer Anwendung, einen Verschlüsselungs-oder Signatur Algorithmus auszuwählen, aber die Implementierung jedes kryptografischen Vorgangs erfolgt durch den CSP.
-   Anwendungen behandeln keine Benutzer [*Anmelde*](../secgloss/c-gly.md) Informationen oder andere Benutzer Authentifizierungsdaten. Die Benutzerauthentifizierung erfolgt durch den CSP. Folglich funktionieren zukünftige CSPs mit erweiterten Authentifizierungsfunktionen, wie z. b. biometrische Eingaben,, ohne dass das Anwendungs Authentifizierungs Modell geändert werden muss.

Ein CSP besteht mindestens aus einer Dynamic Link Library (dll) und einer [*Signatur Datei*](../secgloss/s-gly.md). Die Signatur Datei ist erforderlich, um sicherzustellen, dass der CSP von der [*kryptografieapi*](../secgloss/c-gly.md) erkannt wird. CryptoAPI überprüft diese Signatur regelmäßig, um sicherzustellen, dass Manipulationen am CSP erkannt werden.

Einige CSPs können einen Bruchteil ihrer Funktionalität in einem Adress getrennten Dienst implementieren, der über das lokale RPC oder durch einen Systemgeräte Treiber aufgerufen wird. Durch das Isolieren von globalen Schlüssel-und zentralen kryptografievorgängen in einem Adress getrennten Dienst oder in einer Hardware werden Schlüssel und Vorgänge vor Manipulationen innerhalb eines Anwendungsdaten Raums geschützt.

Es ist unklug, dass Anwendungen bestimmte Attribute für einen bestimmten CSP nutzen. Beispielsweise unterstützt der Kryptografieanbieter von Microsoft, der mit CryptoAPI bereitgestellt wird, 40-Bit-Sitzungsschlüssel und öffentliche 512-Bit-Schlüssel. Anwendungen, die diese Schlüssel bearbeiten, müssen Annahmen über den Umfang des Arbeitsspeichers vermeiden, der zum Speichern dieser Schlüssel benötigt wird, da die Anwendung wahrscheinlich fehlschlägt, wenn ein anderer CSP verwendet wird. Gut geschriebene Anwendungen müssen mit einer Vielzahl von CSPs funktionieren.

Ausführliche Informationen zu Kryptografieanbietern und vordefinierten CSPs, die mit CryptoAPI verwendet werden können, finden Sie unter [kryptografieanbiettypen](cryptographic-provider-types.md) und [Microsoft-Kryptografiedienstanbieter](microsoft-cryptographic-service-providers.md).

 

 
