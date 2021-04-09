---
description: Der Paket Code ist eine GUID, die ein bestimmtes Windows Installer Paket identifiziert.
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: Paket Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131472"
---
# <a name="package-codes"></a>Paket Codes

Der Paket Code ist eine GUID, die ein bestimmtes Windows Installer [*Paket*](p-gly.md)identifiziert. Der Paket Code ordnet eine MSI-Datei einer Anwendung oder einem Produkt zu und kann auch für die Überprüfung von Quellen verwendet werden. Die Produkt-und Paket Codes sind nicht austauschbar. Weitere Informationen finden Sie unter [Product Codes](product-codes.md).

Nonidentical. msi-Dateien sollten nicht denselben Paket Code aufweisen. Es ist wichtig, den Paket Code zu ändern, da er der primäre Bezeichner ist, der vom Installer verwendet wird, um nach dem richtigen Paket für eine bestimmte Installation zu suchen und dieses zu überprüfen. Wenn ein Paket geändert wird, ohne den Paket Code zu ändern, verwendet das Installationsprogramm ggf. das neuere Paket nicht, wenn auf beide weiterhin für den Installer zugegriffen werden kann.

Der Paketcode wird in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " des [Zusammenfassungs Informationsdaten Stroms](summary-information-stream.md)gespeichert. Beachten Sie, dass Buchstaben in Produktcode und Paket Code-GUIDs Großbuchstaben sein müssen. Dienstprogramme wie GUIDGEN generieren GUIDs, die Kleinbuchstaben enthalten. Die Kleinbuchstaben in diesen GUIDs müssen in Großbuchstaben geändert werden, damit Sie als Produktcode oder Paketcode verwendet werden können.

Obwohl es üblich ist, eine Anwendung zu liefern, die denselben Paketcode und Produktcode aufweist, können sich die beiden Werte beim Aktualisieren der Anwendung unterscheiden. Wenn Sie z. b. eine neue Datei mit der Anwendung einschließen möchten, müssen Sie die Installations Datenbank aktualisieren, um die Datei zu installieren. Wenn die Änderungen geringfügig sind, kann ein Entwickler den Produktcode nicht ändern. es ist jedoch eine andere MSI-Datei erforderlich, um die neue Datei zu installieren. Daher muss der Paketcode erhöht werden. Umgekehrt kann ein einzelnes Paket verwendet werden, um mehr als ein Produkt zu installieren. Beispielsweise könnte bei der Installation eines Pakets ohne eine sprach Transformation die englische Version der Anwendung installiert werden, und bei der Installation desselben Pakets mit einer sprach Transformation könnte die französische Version installiert werden. Die Transformation unterscheidet sich von der MSI-Datei, die den Paket Code bestimmt. Die englische und die französische Version können unterschiedliche Produktcodes und denselben Paket Code aufweisen, da beide mit der gleichen MSI-Datei installiert werden.

 

 



