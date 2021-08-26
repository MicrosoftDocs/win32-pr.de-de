---
description: Autoren von Installationspaketen sollten immer eine Überprüfung für ihre Pakete ausführen, bevor sie versuchen, das Paket zum ersten Mal zu installieren, und die Überprüfung bei jeder Änderung des Pakets erneut ausführen.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Überprüfen einer Installationsdatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d4d1937b5946d6c1df85a4c6c21ec8113ef6463b5aaad0e181f4bdc711e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995820"
---
# <a name="validating-an-installation-database"></a>Überprüfen einer Installationsdatenbank

Autoren von Installationspaketen sollten immer eine Überprüfung für ihre Pakete ausführen, bevor sie versuchen, das Paket zum ersten Mal zu installieren, und die Überprüfung bei jeder Änderung des Pakets erneut ausführen. Bei der Überprüfung wird die Datenbank auf Fehler überprüft, die möglicherweise einzeln gültig erscheinen, aber im Kontext der gesamten Datenbank ein falsches Verhalten verursachen. Der Versuch, ein Paket zu installieren, bei dem die Überprüfung fehlschlägt, kann das System des Benutzers beschädigen. Weitere Informationen finden Sie in [den Abschnitten Paketvalidierung](package-validation.md) und interne [Konsistenzauswertung – ICEs.](internal-consistency-evaluators-ices.md)

Sie können das Beispielpaket [ mithilfe ](orca-exe.md) vonOrca.exe[ oder ](msival2-exe.md)Msival2.exe. Um die Hilfe zum Ändern Msival2.exe, und geben Sie in der Befehlszeile ein.

Ms luci2 -?

Die CUB-Datei darice.cub enthält die benutzerdefinierten ICE-Aktionen, die von Msival2.exe Validierung benötigt werden. So überprüfen Sie die MNP2000.msi Eingabe

msiva2 MNP2000.msi Darice.cub

Eine Beschreibung der von der Validierung zurückgegebenen Fehler- und Warnmeldungen finden Sie in der [ICE-Referenz.](ice-reference.md) Korrigieren Sie alle Fehler im Paket, und führen Sie die Überprüfung nach Bedarf erneut aus, bis das Paket die Überprüfung ohne Fehler besteht.

Sobald das Paket die Überprüfung besteht, können Sie das Beispielpaket installieren, indem Sie auf das Symbol MNP2000.msi klicken oder über die Befehlszeile mithilfe der [Befehlszeilenoptionen .](command-line-options.md)

Dadurch wird die Beispielinstallation abgeschlossen.

## <a name="next-example"></a>Nächstes Beispiel

[Ein Upgradebeispiel](an-upgrade-example.md)

 

 



