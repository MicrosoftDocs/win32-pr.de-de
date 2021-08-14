---
description: Stellt einen Mechanismus zum Steuern des Zugriffs auf sicherungsfähige Objekte bereit.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: bevollmächtigende Integritätskontrolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1a39cfc1d1ab819181e37c17328d6015a884f9ae1cce546643480351341b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781493"
---
# <a name="mandatory-integrity-control"></a>bevollmächtigende Integritätskontrolle

bevollmächtigende Integritätskontrolle (MIC) bietet einen Mechanismus zum Steuern des Zugriffs auf sicherungsfähige Objekte. Dieser Mechanismus wird zusätzlich zur diskreten Zugriffssteuerung durchgeführt und wertet den Zugriff aus, bevor Zugriffsüberprüfungen für die [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) eines Objekts ausgewertet werden.

MIC verwendet Integritätsstufen und obligatorische Richtlinien, um den Zugriff auszuwerten. [*Sicherheitsprinzipalen*](/windows/desktop/SecGloss/s-gly) und sicherungsfähigen Objekten werden Integritätsebenen zugewiesen, die ihre Schutz- oder Zugriffsebenen bestimmen. Beispielsweise kann ein Prinzipal mit einer niedrigen Integritätsebene nicht in ein Objekt mit einer mittleren Integritätsebene schreiben, auch wenn die DACL dieses Objekts Schreibzugriff auf den Prinzipal zulässt.

Windows definiert vier Integritätsebenen: niedrig, mittel, hoch und system. Standardbenutzer erhalten mittlere, benutzer mit erhöhten Rechten eine hohe Benachrichtigung. Prozesse, die Sie starten, und Objekte, die Sie erstellen, erhalten Ihre Integritätsstufe (mittel oder hoch) oder niedrig, wenn die Ebene der ausführbaren Datei niedrig ist. -Systemdienste erhalten Systemintegrität. Objekte ohne Integritätsbezeichnung werden vom Betriebssystem als mittel behandelt. dadurch wird verhindert, dass Code mit niedriger Integrität nicht bezeichnete Objekte ändert. Darüber hinaus stellt Windows sicher, dass Prozesse, die mit einer niedrigen Integritätsebene ausgeführt werden, keinen Zugriff auf einen Prozess erhalten können, der einem App-Container zugeordnet ist.

## <a name="integrity-labels"></a>Integritätsbezeichnungen

Integritätsbezeichnungen geben die Integritätsebenen von sicherungsfähigen Objekten und Sicherheitsprinzipalen an. Integritätsbezeichnungen werden durch [*Integritäts-SIDs*](/windows/desktop/SecGloss/i-gly)dargestellt. Die Integritäts-SID für ein sicherungsfähiges Objekt wird in seiner [*SACL (System Access Control List)*](/windows/desktop/SecGloss/s-gly) gespeichert. Die SACL enthält einen [**ACE (SYSTEM \_ MANDATORY LABEL \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) [*Access Control Entry),*](/windows/desktop/SecGloss/a-gly) der wiederum die Integritäts-SID enthält. Jedes Objekt ohne Integritäts-SID wird so behandelt, als ob es eine mittlere Integrität hätte.

Die Integritäts-SID für einen Sicherheitsprinzipal wird in seinem Zugriffstoken gespeichert. Ein Zugriffstoken kann mindestens eine Integritäts-SIDs enthalten.

Ausführliche Informationen zu den definierten [Integritäts-SIDs](well-known-sids.md)finden Sie unter Bekannte SIDs.

## <a name="process-creation"></a>Prozesserstellung

Wenn ein Benutzer versucht, eine ausführbare Datei zu starten, wird der neue Prozess mit dem Mindestwert der Benutzerintegritätsstufe und der Dateiintegritätsstufe erstellt. Dies bedeutet, dass der neue Prozess nie mit höherer Integrität als die ausführbare Datei ausgeführt wird. Wenn der Administratorbenutzer ein Programm mit niedriger Integrität ausführt, funktioniert das Token für den neuen Prozess mit der niedrigen Integritätsstufe. Dadurch wird ein Benutzer, der nicht vertrauenswürdigen Code startet, vor böswilligen Handlungen geschützt, die von diesem Code ausgeführt werden. Die Benutzerdaten, die sich auf der typischen Benutzerintegritätsebene verhalten, sind vor diesem neuen Prozess schreibgeschützt.

## <a name="mandatory-policy"></a>Obligatorische Richtlinie

Der [**ACE ACE SYSTEM MANDATORY \_ \_ LABEL \_**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) in der SACL eines sicherungsfähigen Objekts enthält eine Zugriffsmaske, die den Zugriff angibt, der Prinzipalen mit niedrigeren Integritätsebenen als dem -Objekt gewährt wird. Die für diese Zugriffsmaske definierten Werte sind **SYSTEM MANDATORY LABEL NO WRITE \_ \_ \_ \_ \_ UP**, **SYSTEM MANDATORY LABEL NO READ \_ \_ \_ \_ \_ UP** und **SYSTEM MANDATORY LABEL NO EXECUTE \_ \_ \_ \_ \_ UP**. Standardmäßig erstellt das System jedes Objekt mit der Zugriffsmaske **SYSTEM MANDATORY LABEL NO WRITE \_ \_ \_ \_ \_ UP**.

Jedes Zugriffstoken gibt auch eine obligatorische Richtlinie an, die von der [*lokalen Sicherheitsautorität (Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) festgelegt wird, wenn das Token erstellt wird. Diese Richtlinie wird durch eine [**TOKEN \_ MANDATORY \_ POLICY-Struktur**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) angegeben, die dem Token zugeordnet ist. Diese Struktur kann durch Aufrufen der [**GetTokenInformation-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) abgefragt werden, wobei der Wert des *TokenInformationClass-Parameters* auf **TokenKategorieoryPolicy** festgelegt ist.

 

 
