---
title: Registrieren von Objekten in rot
description: Registrieren von Objekten in rot
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d77e7bc6fe8b0a4d5896bf33575df2f57fb0e583f78acd02653f6ccb014f34ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104812"
---
# <a name="registering-objects-in-the-rot"></a>Registrieren von Objekten in rot

Wenn ein Client einen Server auffordert, eine Objektinstanz zu erstellen, erstellt der Server in der Regel einen Moniker für das Objekt und registriert es in der laufenden Objekttabelle (ROT) durch einen Aufruf von [**IRunningObjectTable::Register.**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register)

Wenn der Server [**CreateFileMoniker aufruft,**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) um einen Dateimoniker zu erstellen, der in ROT registriert werden soll, sollten Server lokale Dateinamen übergeben, die laufwerksbasiert sind, nicht im UNC-Format. Dadurch wird sichergestellt, dass die vom ROT-Registeraufruf generierten Monikervergleichsdaten mit dem übereinstimmen, was beim Durchführen einer ROT-Suche auf einem Remoteclient verwendet wird. Dies liegt daran, dass die Datei in einen pfadbasierten lokalen Pfad konvertiert wird, wenn der verteilte COM-Dienst eine Aktivierungsanforderung für eine lokale Datei auf dem Server von einem Remoteclient empfängt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installieren als Dienstanwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
</dt> <dt>

[Registrieren eines ausgeführten EXE-Servers](registering-a-running-exe-server.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 




