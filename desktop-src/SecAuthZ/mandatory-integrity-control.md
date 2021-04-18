---
description: Stellt einen Mechanismus zum Steuern des Zugriffs auf Sicherungs fähige Objekte bereit.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: bevollmächtigende Integritätskontrolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c184ba01da0a55309fcb27ace9b0fe156edd6425
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106368271"
---
# <a name="mandatory-integrity-control"></a>bevollmächtigende Integritätskontrolle

Bevollmächtigende Integritätskontrolle (MIC) bietet einen Mechanismus zum Steuern des Zugriffs auf Sicherungs fähige Objekte. Dieser Mechanismus ist zusätzlich zu einer freigegebenen Zugriffs Steuerung und wertet den Zugriff aus, bevor Zugriffs Überprüfungen für die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines Objekts ausgewertet werden.

MIC verwendet Integritäts Ebenen und eine obligatorische Richtlinie zum Auswerten des Zugriffs. [*Sicherheits Prinzipale und Sicherungs*](/windows/desktop/SecGloss/s-gly) fähige Objekte werden Integritäts Ebenen zugewiesen, mit denen die Schutz-oder Zugriffsebenen bestimmt werden. Beispielsweise kann ein Prinzipal mit einer Ebene mit niedriger Integrität nicht in ein Objekt mit mittlerer Integritäts Ebene schreiben, auch wenn die DACL dieses Objekts Schreibzugriff auf den Prinzipal zulässt.

Windows definiert vier Integritäts Ebenen: niedrig, Mittel, hoch und System. Standard Benutzer erhalten mittlere, erhöhte Benutzer mit erhöhten Rechten. Prozesse, die Sie starten, und von Ihnen erstellte Objekte erhalten Ihre Integritäts Stufe (Mittel oder hoch) oder niedrig, wenn die Ebene der ausführbaren Datei niedrig ist. Systemdienste erhalten Systemintegrität. Objekte, die keine Integritäts Bezeichnung besitzen, werden vom Betriebssystem als Mittel behandelt. Dadurch wird verhindert, dass nicht beschriftete Objekte durch Code mit niedriger Integrität geändert werden. Darüber hinaus stellt Windows sicher, dass Prozesse, die mit einer niedrigen Integritäts Stufe ausgeführt werden, keinen Zugriff auf einen Prozess erhalten können, der einem App-Container zugeordnet ist.

## <a name="integrity-labels"></a>Integritäts Bezeichnungen

Integritäts Bezeichnungen geben die Integritäts Ebenen von Sicherungs fähigen Objekten und Sicherheits Prinzipale an. Integritäts Bezeichnungen werden durch [*Integritäts-SIDs*](/windows/desktop/SecGloss/i-gly)dargestellt. Die Integritäts-sid für ein Sicherungs fähiges Objekt wird in der [*System-Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) gespeichert. Die SACL enthält ein [**System \_ obligatorisches " \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE)", das wiederum die Integritäts-sid enthält. Jedes Objekt ohne Integritäts-sid wird so behandelt, als ob es eine mittlere Integrität hätte.

Die Integritäts-sid für einen Sicherheits Prinzipal wird in Ihrem Zugriffs Token gespeichert. Ein Zugriffs Token kann eine oder mehrere Integritäts-SIDs enthalten.

Ausführliche Informationen zu den definierten Integritäts-SIDs finden Sie unter [Bekannte SIDs](well-known-sids.md).

## <a name="process-creation"></a>Prozesserstellung

Wenn ein Benutzer versucht, eine ausführbare Datei zu starten, wird der neue Prozess mit mindestens der Benutzer Integritäts Stufe und der Datei Integritäts Ebene erstellt. Dies bedeutet, dass der neue Prozess nie mit höherer Integrität ausgeführt wird als die ausführbare Datei. Wenn der Administrator Benutzer ein Programm mit niedriger Integrität ausführt, funktioniert das Token für den neuen Prozess mit der Ebene mit niedriger Integrität. Dadurch wird verhindert, dass ein Benutzer, der nicht vertrauenswürdigen Code ausführt, von böswilligen, von diesem Code ausgeführten Aktionen Die Benutzerdaten, bei denen es sich um eine typische Benutzer Integritäts Stufe handelt, sind für diesen neuen Prozess schreibgeschützt.

## <a name="mandatory-policy"></a>Obligatorische Richtlinie

Das [**System \_ erforderliche \_ Label \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) ACE in der SACL eines Sicherungs fähigen Objekts enthält eine Zugriffs Maske, die den Zugriff angibt, mit dem Prinzipale mit Integritäts Ebenen, die niedriger sind als das Objekt, erteilt werden. Bei den für diese Zugriffs Maske definierten Werten handelt es sich um **\_ eine System obligatorische \_ Bezeichnung " \_ kein \_ Schreibvorgang \_**", **\_ eine obligatorische \_ Bezeichnung \_ \_ \_** für das System und eine **\_ obligatorische \_ Bezeichnung " \_ kein \_ Ausführen \_**". Standardmäßig erstellt das System jedes-Objekt mit einer Zugriffs Maske der **obligatorischen Bezeichnung "System" \_ \_ \_ ohne \_ Schreibvorgang \_**.

Jedes Zugriffs Token gibt auch eine obligatorische Richtlinie an, die von der [*lokalen Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) festgelegt wird, wenn das Token erstellt wird. Diese Richtlinie wird durch eine [**\_ verbindliche \_ tokenrichtlinienstruktur**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) angegeben, die dem Token zugeordnet ist. Diese Struktur kann durch Aufrufen der [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -Funktion mit dem Wert des *tokeninformationclass* -Parameters, der auf **tokenmandatorypolicy** festgelegt ist, abgefragt werden.

 

 
