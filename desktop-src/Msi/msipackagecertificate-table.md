---
description: In der Tabelle MsiPackageCertificate werden digitale Signaturzertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die diese Multiple-Package werden.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: MsiPackageCertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62abfa23f5e86949d6254ab89f7d70f01a8a4a8fe138a4eba114d2a45559390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944518"
---
# <a name="msipackagecertificate-table"></a>MsiPackageCertificate-Tabelle

In der Tabelle MsiPackageCertificate sind digitale Signaturzertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die diese Installation mit mehreren [Paketen erstellen.](multiple-package-installations.md)

Verwenden Sie diese Tabelle, um eine Installation mit mehreren [Paketen für](multiple-package-installations.md) ein Produkt zu erstellen, das Windows Installer-Pakete enthält. Wenn das erste Paket digital signiert ist und eine MsiPackageCertificate-Tabelle enthält, in der digitale Zertifikate für alle verbleibenden Pakete im Produkt angegeben sind, muss der Administrator nur die Für das erste Paket angezeigte Eingabeaufforderung benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) akzeptieren. Nachdem die Eingabeaufforderung der Benutzerkontensteuerung für das erste Paket akzeptiert wurde, können die benutzerdefinierten Funktionen in der [Tabelle MsiEmbeddedChainer](msiembeddedchainer-table.md) die restlichen Pakete mit der Installation mehrerer Pakete verbinden, ohne eine UAC-Eingabeaufforderung anzuzeigen und eine Administratorantwort für jedes Paket zu erfordern.

Wenn eine oder mehrere Funktionen in der [MsiEmbeddedChainer-Tabelle](msiembeddedchainer-table.md) ein nicht signiertes Paket anfordern, wird für jedes nicht signierte Paket eine weitere UAC-Eingabeaufforderung angezeigt, die eine Administratorinteraktion erfordert. Wenn der Administrator diese UAC-Eingabeaufforderung akzeptiert, wird die Installation mit mehreren Paketen fortgesetzt. Nachdem ein Administrator Anmeldeinformationen für ein Paket angegeben hat, wird während dieser Installation mit mehreren Paketen keine UAC-Eingabeaufforderung mehr für dieses Paket angezeigt. Wenn der Administrator eine UAC-Eingabeaufforderung für ein Paket ablehnt, führt das Windows-Installationsprogramm ein Rollback für die Installation mit mehreren Paketen aus, bevor ein Commit für die Installation von Paketen ausgeführt wird, die zum Produkt gehören.

**[Windows Installer 4.0 oder früher:](not-supported-in-windows-installer-4-0.md)** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 4.5 verfügbar.

Die MsiPackageCertificate-Tabelle enthält die folgenden Spalten:



| Spalte               | Typ                         | Key | Nullwerte zulässig |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [Identifier](identifier.md) | J   | N        |
| DigitalCertificate\_ | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

Der eindeutige Bezeichner für diese Zeile in der Tabelle MsiPackageCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [MsiDigitalCertificate-Tabelle.](msidigitalcertificate-table.md) Die in der Tabelle MsiDigitalCertificate angegebene Zeile enthält die binäre Darstellung des Signiererzertifikats.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MsiEmbeddedChainer](msiembeddedchainer-table.md)
</dt> <dt>

[MsiDigitalCertificate-Tabelle](msidigitalcertificate-table.md)
</dt> </dl>

 

 



