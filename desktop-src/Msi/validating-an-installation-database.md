---
description: Autoren von Installationspaketen sollten immer die Validierung Ihrer Pakete ausführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren, und die Überprüfung erneut ausführen, wenn Sie Änderungen am Paket vornehmen.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Überprüfen einer Installations Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861892"
---
# <a name="validating-an-installation-database"></a>Überprüfen einer Installations Datenbank

Autoren von Installationspaketen sollten immer die Validierung Ihrer Pakete ausführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren, und die Überprüfung erneut ausführen, wenn Sie Änderungen am Paket vornehmen. Die Validierung scannt die Datenbank auf Fehler, die möglicherweise einzeln angezeigt werden, aber ein falsches Verhalten im Kontext der gesamten Datenbank verursachen. Wenn Sie versuchen, ein Paket zu installieren, bei dem die Überprüfung nicht erfolgreich ist, können Sie das System Weitere Informationen finden Sie in den Abschnitten [Package Validation](package-validation.md) und [internal Konsistenz Evaluators-ICES](internal-consistency-evaluators-ices.md).

Sie können das Beispiel Paket mit [Orca.exe](orca-exe.md) oder [Msival2.exe](msival2-exe.md)überprüfen. Zum Anzeigen der Hilfe für Msival2.exe wechseln Sie in die Befehlszeile, und geben Sie ein.

Msival2 -?

Die CUB-Datei "Darice. Cub" enthält die benutzerdefinierten Ice-Aktionen, die Msival2.exe zum Durchführen der Validierung benötigt. So überprüfen Sie die MNP2000.msi EINGABETASTE

msival2 MNP2000.msi Darice. Cub

Eine Beschreibung der von der Validierung zurückgegebenen Fehler-und Warnmeldungen finden Sie in der [Ice-Referenz](ice-reference.md). Korrigieren Sie alle Fehler im Paket, und führen Sie die Überprüfung nach Bedarf erneut aus, bis das Paket die Überprüfung ohne Fehler bestanden hat.

Sobald das Paket die Überprüfung bestanden hat, können Sie das Beispiel Paket installieren, indem Sie auf das MNP2000.msi Symbol oder über die Befehlszeile mit den [Befehlszeilenoptionen](command-line-options.md)klicken.

Dies schließt die Beispiel Installation ab.

## <a name="next-example"></a>Nächstes Beispiel

[Ein upgradebeispiel](an-upgrade-example.md)

 

 



