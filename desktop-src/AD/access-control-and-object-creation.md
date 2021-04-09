---
title: Access Control und Objekt Erstellung
description: Der Active Directory Server kann ein untergeordnetes Objekt nicht erstellen, wenn der Aufrufer nicht über die ADS \_ right \_ DS \_ Create \_ Child für diesen Objekttyp für den übergeordneten Container verfügt.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- AD-Access Control und Objekt Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101399"
---
# <a name="access-control-and-object-creation"></a>Access Control und Objekt Erstellung

Der Active Directory Server kann ein untergeordnetes Objekt nicht erstellen, wenn der Aufrufer nicht über die **ADS \_ right \_ DS \_ Create \_ Child** für diesen Objekttyp für den übergeordneten Container verfügt. Um die Typen von untergeordneten Objekten zu bestimmen, die der Aufrufer in einem Verzeichnis Objekt erstellen kann, lesen Sie das Attribut " **attribuwedchildclasseseffective** " des Objekts.

Wenn Sie die [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) -Methode zum Erstellen eines untergeordneten Objekts verwenden, wird das Objekt erst dann persistent gemacht, wenn [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) für das neue Objekt aufgerufen wird. Zwischen den **Create** -und **SetInfo** -aufrufen kann der Erstellungs Thread Werte in die Eigenschaften des neuen Objekts einfügen. Nachdem der **SetInfo-Befehl** aufgerufen wurde, verfügt der erstellende Thread nicht unbedingt über die Zugriffsrechte, um die Eigenschaften des neuen Objekts festzulegen. Um sicherzustellen, dass der Aufrufer über diese Rechte verfügt, müssen Sie während der Erstellung eine explizite Sicherheits Beschreibung angeben. Die DACL sollte über einen ACE verfügen, der dem Aufrufer die erforderlichen Zugriffsrechte für das Objekt übergibt.

Weitere Informationen zur Zugriffs Steuerung und Objekt Erstellung finden Sie unter [Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte](how-security-descriptors-are-set-on-new-directory-objects.md).

 

 