---
title: Dienstprinzipalnamen
description: Ein Dienst Prinzipal Name (Service Principal Name, SPN) ist ein eindeutiger Bezeichner einer Dienst Instanz.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Dienstprinzipalnamen
- SPN siehe Dienst Prinzipal Namen
- Dienst Prinzipal Name AD
- Dienst Prinzipal Name AD, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858119"
---
# <a name="service-principal-names"></a>Dienstprinzipalnamen

Ein Dienst Prinzipal Name (Service Principal Name, SPN) ist ein eindeutiger Bezeichner einer Dienst Instanz. SPNs werden von der [Kerberos-Authentifizierung](mutual-authentication-using-kerberos.md) verwendet, um eine Dienst Instanz einem Dienst Anmelde Konto zuzuordnen. Dadurch kann eine Client Anwendung anfordern, dass der Dienst ein Konto authentifiziert, auch wenn der Client nicht über den Kontonamen verfügt.

Wenn Sie mehrere Instanzen eines Diensts auf Computern innerhalb einer Gesamtstruktur installieren, muss jede Instanz über einen eigenen SPN verfügen. Eine Dienstinstanz kann mehrere SPNs aufweisen, falls mehrere Namen vorhanden sind, die von den Clients zur Authentifizierung verwendet werden können. Ein SPN enthält z. b. immer den Namen des Host Computers, auf dem die Dienst Instanz ausgeführt wird, sodass eine Dienst Instanz möglicherweise einen SPN für jeden Namen oder Alias des Hosts registriert. Weitere Informationen zum SPN-Format und zum Verfassen eines eindeutigen SPN finden Sie unter [namens Formate für eindeutige SPNs](name-formats-for-unique-spns.md).

Bevor der Kerberos-Authentifizierungsdienst einen SPN zum Authentifizieren eines Dienstanbieter verwenden kann, muss der SPN für das Konto Objekt registriert werden, das von der Dienst Instanz für die Anmeldung verwendet wird. Ein angegebener SPN kann nur für ein Konto registriert werden. Bei Win32-Diensten gibt ein Dienst Installationsprogramm das Anmelde Konto an, wenn eine Instanz des Diensts installiert ist. Der Installer fügt dann die SPNs ein und schreibt Sie als Eigenschaft des Account-Objekts in Active Directory Domain Services. Wenn das Anmelde Konto einer Dienst Instanz geändert wird, müssen die SPNs unter dem neuen Konto neu registriert werden. Weitere Informationen finden Sie unter [wie ein Dienst seine SPNs registriert](how-a-service-registers-its-spns.md).

Wenn ein Client eine Verbindung zu einem Dienst herstellen möchte, sucht er eine Instanz des Diensts, verfasst einen SPN für diese Instanz, stellt eine Verbindung zum Dienst her und übergibt den SPN zur Authentifizierung an den Dienst. Weitere Informationen finden Sie unter [Funktionsweise eines Dienst-SPN durch Clients](how-clients-compose-a-serviceampaposs-spn.md).

## <a name="in-this-section"></a>In diesem Abschnitt

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Namens Formate für eindeutige SPNs](name-formats-for-unique-spns.md)
</dt> <dt>

[Wie ein Dienst seine SPNs verfasst hat](how-a-service-composes-its-spns.md)
</dt> <dt>

[Registrieren der SPNs durch einen Dienst](how-a-service-registers-its-spns.md)
</dt> <dt>

[Funktionsweise eines Dienst-SPN durch Clients](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Was ist ein SPN, und warum sollten Sie sich darauf kümmern?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Gegenseitige Authentifizierung mithilfe von Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 