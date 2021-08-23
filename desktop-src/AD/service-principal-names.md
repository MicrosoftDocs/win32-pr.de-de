---
title: Dienstprinzipalnamen
description: Ein Dienstprinzipalname (Service Principal Name, SPN) ist ein eindeutiger Bezeichner einer Dienstinstanz.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Dienstprinzipalnamen
- SPN siehe Dienstprinzipalnamen
- Dienstprinzipalname AD
- Dienstprinzipalname AD , Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6639ade82f029a89cb378de20bb279348962c4a991899f95e7f1b06157cd7ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024818"
---
# <a name="service-principal-names"></a>Dienstprinzipalnamen

Ein Dienstprinzipalname (Service Principal Name, SPN) ist ein eindeutiger Bezeichner einer Dienstinstanz. SPNs werden von der [Kerberos-Authentifizierung verwendet,](mutual-authentication-using-kerberos.md) um eine Dienstinstanz einem Dienstanmeldungskonto zu zuordnen. Dadurch kann eine Clientanwendung anfordern, dass der Dienst ein Konto authentifiziert, auch wenn der Client nicht über den Kontonamen verfügt.

Wenn Sie mehrere Instanzen eines Diensts auf Computern innerhalb einer Gesamtstruktur installieren, muss jede Instanz über einen eigenen SPN verfügen. Eine Dienstinstanz kann mehrere SPNs aufweisen, falls mehrere Namen vorhanden sind, die von den Clients zur Authentifizierung verwendet werden können. Beispielsweise enthält ein SPN immer den Namen des Hostcomputers, auf dem die Dienstinstanz ausgeführt wird, sodass eine Dienstinstanz einen SPN für jeden Namen oder Alias des Hosts registrieren kann. Weitere Informationen zum SPN-Format und zum Erstellen eines eindeutigen SPN finden Sie unter [Namensformate für eindeutige SPNs.](name-formats-for-unique-spns.md)

Bevor der Kerberos-Authentifizierungsdienst einen SPN zum Authentifizieren eines Diensts verwenden kann, muss der SPN für das Kontoobjekt registriert werden, das die Dienstinstanz für die Anmeldung verwendet. Ein angegebener SPN kann nur für ein Konto registriert werden. Für Win32-Dienste gibt ein Dienstinstallationsprogramm das Anmeldekonto an, wenn eine Instanz des Diensts installiert wird. Das Installationsprogramm erstellt dann die SPNs und schreibt sie als Eigenschaft des Kontoobjekts in Active Directory Domain Services. Wenn sich das Anmeldekonto einer Dienstinstanz ändert, müssen die SPNs unter dem neuen Konto erneut registriert werden. Weitere Informationen finden Sie unter [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).

Wenn ein Client eine Verbindung zu einem Dienst herstellen möchte, sucht er eine Instanz des Diensts, verfasst einen SPN für diese Instanz, stellt eine Verbindung zum Dienst her und übergibt den SPN zur Authentifizierung an den Dienst. Weitere Informationen finden Sie unter [How Clients Compose a Service es SPN](how-clients-compose-a-serviceampaposs-spn.md).

## <a name="in-this-section"></a>In diesem Abschnitt

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Namensformate für eindeutige SPNs](name-formats-for-unique-spns.md)
</dt> <dt>

[So erstellt ein Dienst seine SPNs](how-a-service-composes-its-spns.md)
</dt> <dt>

[So registriert ein Dienst seine SPNs](how-a-service-registers-its-spns.md)
</dt> <dt>

[So erstellen Clients den SPN eines Diensts](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Was ist ein SPN, und warum sollten Sie sich darum kümmern?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Gegenseitige Authentifizierung mithilfe von Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 