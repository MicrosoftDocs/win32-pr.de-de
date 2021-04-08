---
title: Einrichten des Benutzerkontos eines Dienstanbieter
description: Ihr Dienst Installationsprogramm kann ein Standard Anmelde Konto für eine Dienst Instanz vorschlagen und es dem Administrator gestatten, das Standardkonto auszuwählen oder ein anderes Konto anzugeben.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Einrichten des Benutzerkonto-AD eines Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705fa16d8d2cce137755f4a5086716aaaef8046a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724408"
---
# <a name="setting-up-a-services-user-account"></a>Einrichten des Benutzerkontos eines Dienstanbieter

Ihr Dienst Installationsprogramm kann ein Standard Anmelde Konto für eine Dienst Instanz vorschlagen und es dem Administrator gestatten, das Standardkonto auszuwählen oder ein anderes Konto anzugeben. Wenn der Administrator ein Benutzerkonto und nicht das LocalSystem-Konto auswählt, muss das Konto vorhanden sein, bevor Sie die Funktion " [**roateservice**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) " aufrufen, um eine Instanz des Diensts auf einem Host Server zu installieren. Weitere Informationen und ein Codebeispiel, das zum Erstellen eines neuen Domänen Benutzer Objekts in Active Directory Domain Services verwendet werden kann, finden Sie unter [Erstellen eines Benutzers](creating-a-user.md).

Im Idealfall sollte jede Instanz eines Diensts, unabhängig davon, ob es sich um einen Host basierten oder replizierbaren Dienst handelt, über ein eigenes Domänen Benutzerkonto verfügen. Die Verwendung separater Konten für jede Dienst Instanz ist sicherer als bei mehreren Instanzen, die dasselbe Konto gemeinsam verwenden. Die Verwendung separater Konten ermöglicht außerdem das Überwachen der Aktivitäten der einzelnen Dienst Instanzen.

Wenn das Installationsprogramm ein Standard Anmelde Konto vorschlägt, sollte es den Namen eines neuen Kontos angeben, das für die neue Dienst Instanz erstellt werden soll. Der Kontoname kann aus denselben Elementen bestehen, die zum Verfassen eines Dienst Prinzipal namens verwendet werden, wie z. b. die Dienstklasse, der Host Computer und der Dienst Name. Weitere Informationen finden Sie unter [Dienstprinzipalnamen](service-principal-names.md). In der Regel erstellen Sie das Konto im Benutzer Container in der Domäne des Host Computers.

Sie müssen für jedes Konto ein Kennwort generieren. Weitere Informationen zum Schreiben eines Tools, das die Aufgabe der Aktualisierung von Dienst Konto Kennwörtern automatisiert, finden Sie unter [Ändern des Kennworts für das Benutzerkonto eines Dienstanbieter](changing-the-password-on-a-serviceampaposs-user-account.md).

 

 