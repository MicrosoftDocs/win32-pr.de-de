---
title: Registrieren von Objekten in der rot
description: Registrieren von Objekten in der rot
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b452ead94a717791910ecceaa5082535bc1b233c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388358"
---
# <a name="registering-objects-in-the-rot"></a>Registrieren von Objekten in der rot

Wenn ein Client einen Server anfordert, eine Objektinstanz zu erstellen, erstellt der Server in der Regel einen Moniker für das Objekt und registriert ihn in der laufenden Objekttabelle (rot) durch einen Aufruf von " [**iriunningobjec\:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register)".

Wenn der Server " [**kreatefilemoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) " aufruft, um einen dateimoniker zu erstellen, der in der rot registriert werden soll, sollten Server lokale Dateinamen übergeben, die Laufwerk basiert und nicht im UNC-Format sind. Dadurch wird sichergestellt, dass die vom rot-Registrierungs Aufruf generierten Moniker-Vergleichsdaten mit den beim Durchsuchen einer rot-Suche im Teil eines Remote Clients verwendeten Daten verglichen werden. Dies liegt daran, dass der verteilte com-Dienst, wenn er von einem Remote Client eine Aktivierungs Anforderung für eine lokale Datei an den Server empfängt, in einen auf lokalen Laufwerken basierenden Pfad konvertiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installieren von als Dienst Anwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
</dt> <dt>

[Registrieren eines ausführenden exe-Servers](registering-a-running-exe-server.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 




