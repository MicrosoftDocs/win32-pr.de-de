---
description: Wie digitale Zertifikate eine sichere Kommunikation bereitstellen und wie CryptoAPI verwendet wird, um diese Zertifikate zu verwenden und zu verwalten.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Digitale Zertifikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f2df1a529d94fa5a04385c7f91f5aefbb40c0488ef0c5c484fe98c3874358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875300"
---
# <a name="digital-certificates"></a>Digitale Zertifikate

Die Authentifizierung ist entscheidend, um die Kommunikation zu schützen. Benutzer müssen in der Lage sein, ihre Identität gegenüber den Personen nachzuweisen, mit denen sie kommunizieren, und in der Lage sein, die Identität anderer zu überprüfen. Die Authentifizierung der Identität in einem Netzwerk ist sehr komplex, da sich die miteinander kommunizierenden Parteien bei der Kommunikation nicht physisch treffen. Dies kann Personen mit unlauteren Absichten ermöglichen, Nachrichten abzufangen oder eine andere Identität vorzutäuschen. Es muss eine Methode entwickelt werden, um das erforderliche Maß an Vertrauen innerhalb des Kommunikationsprozesses zu erhalten.

Das [*digitale Zertifikat ist*](../secgloss/c-gly.md) eine allgemeine Anmeldeinformation, die eine Möglichkeit zum Überprüfen der Identität bietet. Dieser Abschnitt bietet eine Übersicht darüber, wie Zertifikate eine sichere Kommunikation bereitstellen und wie CryptoAPI verwendet wird, um diese Zertifikate zu verwenden und zu verwalten.

Ein Zertifikat ist ein Satz von Daten, der eine Entität identifiziert. Eine vertrauenswürdige Organisation weist ein Zertifikat einer Einzelperson oder einer Entität zu, die der Person einen öffentlichen Schlüssel zu ordnet. Die Person oder Entität, für die bzw. die ein Zertifikat ausgestellt wird, wird als Der Subjekt dieses Zertifikats bezeichnet. Die vertrauenswürdige Organisation, die das Zertifikat ausstellen, ist eine [*Zertifizierungsstelle*](../secgloss/c-gly.md) und wird als Aussteller des Zertifikats bezeichnet. Eine vertrauenswürdige Zertifizierungsstelle gibt ein Zertifikat erst aus, nachdem die Identität des Zertifikatssubjekts überprüft wurde.

Zertifikate verwenden kryptografische Techniken, um das Problem des fehlenden physischen Kontakts zwischen den Kommunizierenden zu beheben. Die Verwendung dieser Techniken schränkt die Möglichkeit ein, dass eine untypische Person Nachrichten abfing, ändert oder unsind. Diese kryptografischen Techniken erschweren das Ändern von Zertifikaten. Daher ist es für eine Entität schwierig, die Identität einer anderen Person zu imitieren.

Die Daten in einem Zertifikat enthalten den öffentlichen kryptografischen Schlüssel aus dem Paar aus öffentlichem [*und privatem Schlüssel des Zertifikatssubjekts.*](../secgloss/p-gly.md) Eine Nachricht, die mit dem privaten Schlüssel des Absenders signiert wurde, kann nur vom Empfänger der Nachricht mithilfe des öffentlichen Schlüssels des Absenders abgerufen werden. Diesen Schlüssel finden Sie in einer Kopie des Zertifikats des Absenders. Das Abrufen einer Signatur mit einem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) aus einem Zertifikat zeigt, dass die Signatur mit dem privaten Schlüssel des Zertifikatssubjekts [*erstellt wurde.*](../secgloss/p-gly.md) Wenn der Absender sehr vorsichtig war und den geheimen Schlüssel des privaten Schlüssels aufbewahrt hat, kann der Empfänger sicher sein, dass er die Identität des Absenders der Nachricht hat.

In einem Netzwerk gibt es häufig eine vertrauenswürdige Anwendung, die als [*Zertifikatserver bezeichnet wird.*](../secgloss/c-gly.md) Eine Zertifizierungsstelle, die auf einem sicheren Computer ausgeführt wird, verwaltet den Zertifikatserver. Diese Anwendung hat Zugriff auf den öffentlichen Schlüssel aller Clients. Zertifikatserver geben Nachrichten aus, die als Zertifikate bezeichnet werden, von denen jedes den öffentlichen Schlüssel eines seiner Clientbenutzer enthält. Jedes Zertifikat wird mit dem privaten Schlüssel der Zertifizierungsstelle signiert. Daher kann der Empfänger eines solchen Zertifikats überprüfen, ob eine angegebene Zertifizierungsstelle es gesendet hat.

Digitale Zertifikate enthalten auch Erweiterungen und erweiterte Eigenschaften, die zusätzliche Informationen über den Betreff des Zertifikats bereitstellen, z. B. die E-Mail-Adresse des Subjekts und die Aktivitäten, die der Subjekt des Zertifikats ausführen kann.

 

 
