---
description: Die Art und Weise, wie die digitalen Zertifikate eine sichere Kommunikation bieten und wie die kryptoapi verwendet wird, um diese Zertifikate zu verwenden
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Digitale Zertifikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161d200a0f8cab61594872f5182786a3e6597187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750904"
---
# <a name="digital-certificates"></a>Digitale Zertifikate

Die Authentifizierung ist entscheidend für die sichere Kommunikation. Benutzer müssen in der Lage sein, Ihre Identität den Benutzern nachzuweisen, mit denen Sie kommunizieren, und müssen in der Lage sein, die Identität anderer Benutzer zu überprüfen. Die Authentifizierung der Identität in einem Netzwerk ist sehr komplex, da sich die miteinander kommunizierenden Parteien bei der Kommunikation nicht physisch treffen. Dies kann Personen mit unlauteren Absichten ermöglichen, Nachrichten abzufangen oder eine andere Identität vorzutäuschen. Eine Methode muss zusammengearbeitet werden, um die erforderliche Vertrauens Ebene innerhalb des Kommunikations Vorgangs aufrechtzuerhalten.

Bei dem [*digitalen Zertifikat*](../secgloss/c-gly.md) handelt es sich um allgemeine Anmelde Informationen, die eine Möglichkeit zum Überprüfen der Identität bereitstellen. Dieser Abschnitt bietet eine Übersicht darüber, wie Zertifikate eine sichere Kommunikation bereitstellen und wie die kryptoapi verwendet wird, um diese Zertifikate zu verwenden und zu verwalten.

Ein Zertifikat ist eine Gruppe von Daten, die eine Entität identifiziert. Eine vertrauenswürdige Organisation weist eine Person oder eine Entität zu, die einen öffentlichen Schlüssel der Person zuordnet. Die Person oder Entität, für die ein Zertifikat ausgestellt wird, wird als Betreff dieses Zertifikats bezeichnet. Die vertrauenswürdige Organisation, die das Zertifikat ausgibt, ist eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) und wird als Aussteller des Zertifikats bezeichnet. Eine vertrauenswürdige Zertifizierungsstelle stellt nur dann ein Zertifikat aus, nachdem die Identität des Zertifikats überprüft wurde.

Zertifikate verwenden kryptografische Techniken, um das Problem des Mangels an physischem Kontakt zwischen den Kommunikation zu beheben. Durch die Verwendung dieser Techniken wird die Gefahr eingeschränkt, dass eine unethische Person Nachrichten abfängt, ändert oder Fälschungs Fehler durchsetzt. Diese kryptografischen Techniken erschweren das Ändern von Zertifikaten. Daher ist es für eine Entität schwierig, die Identität eines anderen Benutzers anzunehmen.

Die Daten in einem Zertifikat enthalten den öffentlichen kryptografischen Schlüssel aus dem [*öffentlichen/privaten Schlüsselpaar*](../secgloss/p-gly.md)des Zertifikats. Eine Nachricht, die mit dem privaten Schlüssel des Absenders signiert ist, kann nur vom Empfänger der Nachricht mit dem öffentlichen Schlüssel des Absenders abgerufen werden. Dieser Schlüssel befindet sich in einer Kopie des Absender Zertifikats. Wenn Sie eine Signatur mit einem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) aus einem Zertifikat abrufen, wird bestätigt, dass die Signatur mit dem [*privaten Schlüssel*](../secgloss/p-gly.md)des Zertifikat Antragstellers erstellt wurde. Wenn der Absender wachsam war und den geheimen Schlüssel des privaten Schlüssels beibehalten hat, kann der Empfänger die Identität des Absender der Nachricht vertrauen.

In einem Netzwerk gibt es häufig eine vertrauenswürdige Anwendung, die als [*Zertifikat Server*](../secgloss/c-gly.md)bezeichnet wird. Eine Zertifizierungsstelle, die auf einem sicheren Computer ausgeführt wird, verwaltet den Zertifikat Server. Diese Anwendung hat Zugriff auf den öffentlichen Schlüssel aller Clients. Zertifikat Server können Nachrichten ausgeben, die als Zertifikate bezeichnet werden, von denen jeder den öffentlichen Schlüssel eines seiner Client Benutzer enthält. Jedes Zertifikat wird mit dem privaten Schlüssel der Zertifizierungsstelle signiert. Daher kann der Empfänger eines solchen Zertifikats überprüfen, ob er von einer angegebenen Zertifizierungsstelle gesendet wurde.

Digitale Zertifikate enthalten außerdem Erweiterungen und erweiterte Eigenschaften, die zusätzliche Informationen zum Betreff des Zertifikats bereitstellen, z. b. die e-Mail-Adresse des Antragstellers und die Aktivitäten, die der Betreff des Zertifikats ausführen kann.

 

 
