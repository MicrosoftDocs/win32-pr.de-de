---
description: Registrieren und Aufheben der Registrierung von Schlüsseln
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrieren und Aufheben der Registrierung von Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d586fc2bf399a30b8a962611a21a4e0994d88f4513453c071b110de1d4142b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612163"
---
# <a name="registering-and-deregistering-keys"></a>Registrieren und Aufheben der Registrierung von Schlüsseln

## <a name="registering-keys"></a>Registrieren von Schlüsseln

Ein Knoten kann Schlüssel jederzeit bei [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) registrieren, während er sich in den Zuständen **DRT \_ ACTIVE,** **DRT \_ ALONE** und **DRT \_ NO \_ NETWORK** befindet. Schlüssel, die im **DRT \_ ALONE-** und **DRT \_ NO \_ NETWORK-Status** registriert sind, können von anderen DRTs erst erkannt werden, nachdem der lokale Knoten auf **DRT \_ ACTIVE** umgestellt wurde.

Identische Schlüssel können nicht innerhalb derselben DRT-Instanz registriert werden, wenn [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider)verwendet wird. Wenn versucht wird, identische Schlüssel zu registrieren, schlägt die Registrierung des zweiten Schlüssels fehl. Die Verwendung identischer Schlüssel sollte auch zwischen verschiedenen DRT-Instanzen vermieden werden. Suchvorgänge nach der eindeutigen Schlüsselbezeichnung diese identische Schlüsselfreigabe kann einen der Schlüssel zurückgeben, unabhängig davon, welche Daten dem Schlüssel zugeordnet sind.

> [!Note]  
> Wenn für die Implementierung ein anderes Verhalten erforderlich ist, kann anstelle von [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) ein Sicherheitsanbieter erstellt werden, um dies zu ermöglichen.

 

## <a name="deregistering-keys"></a>Aufheben der Registrierung von Schlüsseln

Ein Knoten kann die Registrierung eines Schlüssels jederzeit aufheben, nachdem er registriert wurde. Die Registrierung kann jedoch nur von der Anwendung aufgehoben werden, die den Schlüssel registriert hat. Eine Anwendung kann die Registrierung eines Schlüssels beim lokalen Knoten mithilfe der [**DrtUnregisterKey-Funktion**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) aufheben. Nach Abschluss des Vorgangs löst die Funktion ein **DRT \_ EVENT \_ LEAFSET \_ KEY \_ CHANGE-Ereignis** aus und informiert die Anwendung sowie andere Knoten, die am DRT-Netz beteiligt sind.

Im **DRT \_ FAULTED-Zustand** führt der erforderliche Aufruf von [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) dazu, dass die REGISTRIERUNG aller Schlüssel durch die DRT-Infrastruktur aufgehoben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchsuchen einer verteilten Routingtabelle](searching-a-distributed-routing-table.md)
</dt> <dt>

[Informationen zu verteilten Routingtabellen](about-distributed-routing-tables.md)
</dt> <dt>

[Distributed Routing Tabellen-API Reference](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



