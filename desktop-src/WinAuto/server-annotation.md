---
title: Server Anmerkung
description: Dieser Abschnitt enthält Informationen zur Verwendung der Server Anmerkung.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036572"
---
# <a name="server-annotation"></a>Server Anmerkung

Dieser Abschnitt enthält Informationen zur Verwendung der Server Anmerkung.

## <a name="summary"></a>Zusammenfassung

Sie definieren eine Klasse, die [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)implementiert, eine Instanz davon erstellt und dem System mitteilt, dass Sie bestimmte Eigenschaften für bestimmte UI-Elemente überschreiben möchten. Wenn ein Client eine der Eigenschaften von einem der Benutzeroberflächen Elemente anfordert, wird das Objekt aufgerufen und erhält die Möglichkeit, einen Wert anzugeben. Wenn das Objekt einen Wert zurückgibt, wird dieser Wert an den Client zurückgegeben. Wenn das Objekt keinen Wert zurückgibt, wird der Standardwert für dieses UI-Element an den Client zurückgegeben.

## <a name="when-to-use-this-technique"></a>Verwendungszwecke dieser Technik

Verwenden Sie dieses Verfahren, wenn Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften für ein Objekt überschreiben möchten. Diese Methode ist viel einfacher als vorherige **IAccessible** -Techniken. Weitere Informationen finden Sie unter [Alternativen zur dynamischen Anmerkung](alternatives-to-dynamic-annotation.md).

Sie können die-Server Anmerkung nicht verwenden, um die verfügbar gemachte Objektstruktur zu ändern. Um die Struktur eines Objekts zu ändern, müssen Sie einen vollständigen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger implementieren.

Weitere Informationen zur Server Anmerkung finden Sie in den folgenden Themen:

-   [Verwenden der Server Anmerkung](using-server-annotation.md)
-   [Beispiel für eine Server Anmerkung](server-annotation-sample.md)

 

 




