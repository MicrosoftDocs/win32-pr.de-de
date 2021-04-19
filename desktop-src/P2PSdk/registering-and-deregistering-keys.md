---
description: Registrieren und Aufheben der Registrierung von Schlüsseln
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrieren und Aufheben der Registrierung von Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373191"
---
# <a name="registering-and-deregistering-keys"></a>Registrieren und Aufheben der Registrierung von Schlüsseln

## <a name="registering-keys"></a>Schlüssel werden registriert

Ein Knoten kann jederzeit Schlüssel mit [**drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) registrieren, während er in der **DRT \_ aktiv**, **DRT \_ allein** und **DRT \_ keine \_ Netzwerk** Zustände hat. Schlüssel, die in **DRT \_ allein** registriert sind, und **DRT \_ keine \_ Netzwerk** Zustände, können nur von anderen DRTs erkannt werden, nachdem der lokale Knoten auf **DRT \_ aktiv** umgestellt wurde.

Identische Schlüssel können nicht in derselben DRT-Instanz registriert werden, wenn [**drtkreatederivedkeysecurityprovider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider)verwendet wird. Wenn die Registrierung identischer Schlüssel versucht wird, tritt ein Fehler bei der Registrierung des zweiten Schlüssels auf. Die Verwendung identischer Schlüssel sollte auch zwischen verschiedenen DRT-Instanzen vermieden werden. Durchsuchen anhand der eindeutigen Schlüssel Bezeichnung, die diese identische schlüsselfreigabe hat, kann jeder der Schlüssel zurückgegeben werden, unabhängig davon, welche Daten dem Schlüssel zugeordnet sind.

> [!Note]  
> Wenn für die Implementierung ein anderes Verhalten erforderlich ist, kann ein Sicherheitsanbieter anstelle von [**drtkreatederivedkeysecurityprovider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) erstellt werden, um dies zu ermöglichen.

 

## <a name="deregistering-keys"></a>Aufheben der Registrierung von Schlüsseln

Ein Knoten kann einen Schlüssel jederzeit registrieren, nachdem er registriert wurde. Es kann jedoch nur von der Anwendung, die den Schlüssel registriert hat, die Registrierung aufgehoben werden. Eine Anwendung kann einen Schlüssel aus dem lokalen Knoten mithilfe der [**drtunregisterkey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) -Funktion aufheben. Nach Abschluss löst die Funktion ein Ereignis Änderungs Ereignis für das **DRT- \_ Ereignis \_ Blatt \_ \_** aus und informiert die Anwendung sowie andere Knoten, die am DRT-Mesh teilnehmen.

Im **DRT- \_ Faulted** -Status führt der erforderliche Aufrufe von [**drtclose**](/windows/desktop/api/drt/nf-drt-drtclose) dazu, dass die DRT-Infrastruktur alle Schlüssel Aufhebung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchsuchen einer verteilten Routing Tabelle](searching-a-distributed-routing-table.md)
</dt> <dt>

[Informationen zu verteilten Routing Tabellen](about-distributed-routing-tables.md)
</dt> <dt>

[Tabellen-API Referenz zu verteiltem Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



