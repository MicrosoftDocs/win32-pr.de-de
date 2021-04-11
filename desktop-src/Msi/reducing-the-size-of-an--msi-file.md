---
description: Entwickler von Windows Installer Paketen bemerken möglicherweise, dass Ihre MSI-Dateien nach wiederholten Änderungen und speichern größer als erwartet werden.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reduzieren der Größe einer MSI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959659"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Reduzieren der Größe einer MSI-Datei

Entwickler von Windows Installer Paketen bemerken möglicherweise, dass Ihre MSI-Dateien nach wiederholten Änderungen und speichern größer als erwartet werden. Windows Installer. msi-Dateien sind Verbund Dateien, die Speicher und Streams enthalten und einige der gleichen Speicher Einschränkungen wie OLE-Dokument Dateien aufweisen. Wenn Sie dieselbe MSI-Datei immer wieder bearbeiten und speichern, wird in der Dateispeicher Platz verschwendet. Dies betrifft nur Autoren von MSI-Dateien und hat keine Auswirkung auf Windows Installer Benutzer. Entwickler möchten diesen Speicherplatz möglicherweise entfernen, bevor Sie Ihre abschließende MSI-Datei versenden.

Wenn Sie vergeudeten Speicherplatz entfernen und die endgültige Größe von MSI-Dateien verringern möchten, haben Sie die folgenden Optionen.

-   Exportieren Sie alle Tabellen in der-Datenbank in IDT-Dateien, und importieren Sie Sie dann in eine neue Datenbank. Dadurch wird der kompakteste Speicherplatz erzeugt.
-   Verwenden Sie ein Software Dienstprogramm, um den Speicherplatz von OLE-Dokument Dateien zu komprimieren.

 

 



