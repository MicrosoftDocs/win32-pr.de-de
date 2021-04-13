---
title: Hilfstoken für Bits-Übertragungs Aufträge
description: Hilfstoken für Bits-Übertragungs Aufträge
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52925a6e0d5a9601e21848d514214bfb843f6246
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474196"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Hilfstoken für Bits-Übertragungs Aufträge

In Windows Vista kann eine Anwendung mit dem Background Intelligent Transfer Service-Dienst (Bits) einem Bits-Übertragungs Auftrag ein einzelnes Sicherheits Token zuordnen. Der Bits-Übertragungs Auftrag verwendet dann dieses Token für die Authentifizierung und für den Zugriff auf lokale Ressourcen und Remote Ressourcen.

In Windows 7 ordnet der BITS-Dienst einem Bits-Übertragungs Auftrag ein zusätzliches Token zu. Der Bits-Übertragungs Auftrag kann mit einem zusätzlichen Sicherheits Token konfiguriert werden, bei dem es sich um ein Identitätswechsel Token handelt, das von einer Anwendung erstellt wird, die die Bits com-API aufrufen Dieses hilfstokenmodell ermöglicht es Anwendungen, gleichzeitig zwei verschiedene Sicherheits Token für den Zugriff auf lokale Dateien, Client seitige Zertifikate, Remote Dateien und Proxys zu verwenden. Beispielsweise wird ein Bits-Übertragungs Auftrag erstellt, mit dem die heruntergeladenen Daten in ein privilegiertes lokales Verzeichnis geschrieben und dann eine Domänen Identität mit geringen Rechten für den HTTP-Server und den Proxy Server bereitstellt wird.

Eine Anwendung, in der Regel ein Windows-Dienst, gibt mithilfe der neuen Schnittstelle [**ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)ein Hilfsobjekt an. Diese Schnittstelle wird vom Bits-Auftrags Objekt implementiert. Die Anwendung ruft [**ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) auf, um den Schnittstellen Zeiger zu erhalten. Die Anwendung nimmt die Identität der hilfsidentität an und ruft [**ibitstokenoptions:: sethelpertoken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) auf, um das Token an den Bits-Dienst zu übergeben. Anschließend gibt die Anwendung die Ressourcen an, auf die das Token angewendet wird, indem Sie einen Satz von Bitflags mithilfe von [**ibitstokenoptions:: sethelpertokenflags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags)übergibt. Die Anwendung löscht alle Flags (mit **sethelperonkenflags** ), um das Verhalten wiederherzustellen. Der BITS-Dienst speichert die Bitflags und das Token im Bits-Übertragungs Auftrag.

Wenn sich der Besitzer der Bits-Übertragungs Aufträge anmeldet, verwirft der BITS-Dienst alle Hilfstoken, die dem Übertragungs Auftrag zugeordnet sind. Wenn die Übertragung nicht durchgeführt wird, versetzt der BITS-Dienst den Auftrag in einen Fehlerzustand, während der Fehlercode für die **BG \_ E- \_ Token \_ erforderlich** ist, und verwirft das Hilfstoken. Die Client Anwendung kann das Token durch Aufrufen von [**ibitstokenoptions:: sethelpertoken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) aktualisieren und dann den Bits-Übertragungs Auftrag fortsetzen. Alternativ kann die Client Anwendung die hilfstokenflags mithilfe von [**ibitstokenoptions:: sethelpertokenflags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) löschen und den Übertragungs Auftrag ohne ein Hilfsobjekt fortsetzen.

Wenn sich der Besitzer einer Terminaldienste-Sitzung abmeldet, muss der BITS-Dienst alle Hilfsobjekte dieser Sitzung verwerfen und die betroffenen Übertragungs Aufträge in einem Fehlerzustand mit dem Fehlercode " **BG \_ E \_ Token \_ Required** " platzieren.

Das hilfstokenmodell erfordert eine Änderung an der Bits-Zugriffs Steuerungs Richtlinie. In früheren Versionen von Bits wurden Zugriffs Überprüfungen für jeden Methodenaufrufe implementiert. Ab Windows 7 muss die Zugriffs Überprüfung innerhalb des [**ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Aufrufes ausgeführt werden. Andernfalls hat das Hilfsobjekt möglicherweise keinen Zugriff auf den Übertragungs Auftrag.

> [!Note]  
> Ältere Implementierungen erforderten effektiv, dass Bits-Benutzer über Administratorrechte verfügen, um Hilfstoken festzulegen. Ab Windows 10, Version 1607, können Benutzer, die nicht Administratoren sind, [**ibitstokenoptions:: sethelpertoken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) verwenden, um nicht-Administrator-hilfstokentoken für BITS-Aufträge festzulegen, die Sie besitzen. Diese Änderung ermöglicht es Benutzern, die keine Administratoren sind (z. b. Hintergrund-Download Dienste, die unter dem [Network Service-Konto](/windows/desktop/Services/networkservice-account)ausgeführt werden), Hilfstoken festzulegen.
>
> Insbesondere wurde die Implementierung so geändert, dass Benutzer ohne Administratorrechte Hilfstoken festlegen können, sofern die folgenden Bedingungen erfüllt sind:
>
> -   während des [**ibackgroundcopyjob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Aufrufes ist die SID des Thread Token des Aufrufers identisch mit der SID des Benutzerkontos des Auftrags Besitzers.
> -   beim Aufrufen von [**ibitstokenoptions::**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) "" wird das Hilfsobjekt nicht die Administrator-sid ("**Domänenalias- \_ \_ \_ Admins**") aktiviert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 