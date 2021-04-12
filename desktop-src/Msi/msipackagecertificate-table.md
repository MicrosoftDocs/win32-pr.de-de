---
description: In der Tabelle msipackagecertificate sind digitale Signatur Zertifikate aufgeführt, die zum Überprüfen der Identität der Installationspakete verwendet werden, die diese Multiple-Package der Installation machen.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Msipackagecertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218532"
---
# <a name="msipackagecertificate-table"></a>Msipackagecertificate-Tabelle

In der Tabelle msipackagecertificate sind digitale Signatur Zertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die diese [Installation mit mehreren Paketen](multiple-package-installations.md)vornehmen.

Verwenden Sie diese Tabelle, um eine [Installation mit mehreren](multiple-package-installations.md) Paketen für ein Produkt zu erstellen, das mehrere Windows Installer Pakete enthält. Wenn das erste Paket digital signiert ist und eine msipackagecertificate-Tabelle enthält, die digitale Zertifikate für alle verbleibenden Pakete im Produkt angibt, muss der Administrator nur die Eingabeaufforderung für die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) akzeptieren, die für das erste Paket angezeigt wird. Nachdem die Eingabeaufforderung der Benutzerkontensteuerung für das erste Paket angenommen wurde, können die benutzerdefinierten Funktionen in der [Tabelle msiembeddedchainer](msiembeddedchainer-table.md) die verbleibenden Pakete in die Installation mit mehreren Paketen einbinden, ohne dass eine UAC-Eingabeaufforderung angezeigt wird und für jedes Paket eine Administrator Antwort erforderlich ist.

Wenn eine oder mehrere Funktionen in der [msiembeddedchainer-Tabelle](msiembeddedchainer-table.md) ein nicht signiertes Paket anfordern, wird für jedes nicht signierte Paket eine andere UAC-Eingabeaufforderung angezeigt, die eine Administrator Interaktion erfordert. Wenn der Administrator diese UAC-Eingabeaufforderung annimmt, wird die Multi-Package-Installation fortgesetzt. Wenn ein Administrator die Anmelde Informationen für ein Paket eingegeben hat, wird während der Installation des Multi-Pakets für das Paket keine UAC-Eingabeaufforderung angezeigt. Wenn der Administrator eine UAC-Eingabeaufforderung für ein Paket ablehnt, führt Windows Installer ein Rollback der multipaketinstallation aus, bevor es einen Commit für die Installation der Pakete ausführt, die zum Produkt gehören.

**[Windows Installer 4,0 oder früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 4,5 verfügbar.

Die msipackagecertificate-Tabelle weist die folgenden Spalten auf:



| Spalte               | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------------|------------------------------|-----|----------|
| Packagecertificate   | [Bezeichner](identifier.md) | J   | N        |
| Digitalcertificate\_ | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>Packagecertificate
</dt> <dd>

Der eindeutige Bezeichner für diese Zeile in der msipackagecertificate-Tabelle.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>Digitalcertificate
</dt> <dd>

Ein externer Schlüssel in die erste Spalte der [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md). Die in der Tabelle "msidigitalcertificate" angegebene Zeile enthält die binäre Darstellung des Signatur Geber Zertifikats.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Msiembeddecodchainer](msiembeddedchainer-table.md)
</dt> <dt>

[Msidigitalcertificate-Tabelle](msidigitalcertificate-table.md)
</dt> </dl>

 

 



