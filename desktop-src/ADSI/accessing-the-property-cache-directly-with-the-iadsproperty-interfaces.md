---
title: Zugreifen auf den Eigenschaften Cache mit iadsproperty-Schnittstellen
description: Die iadsproperty-Schnittstellen bestehen aus IADsPropertyList, iadspropertyentry und iadspropertyvalue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Direktes Zugreifen auf den Eigenschaften Cache mit iadsproperty-Schnittstellen ADSI
- Eigenschafts Cache-ADSI
- Eigenschaften Cache-ADSI, verwenden von iadsproperty-Schnittstellen für den Zugriff auf den Eigenschaften Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "103948345"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Zugreifen auf den Eigenschaften Cache mit iadsproperty-Schnittstellen

Die [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) -Schnittstellen bestehen aus [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)und [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue). Diese Schnittstellen stellen Methoden bereit, um direkt auf die Eigenschaften eines Objekt Caches zuzugreifen und diese zu bearbeiten. Eine Eigenschaft wird als Eigenschaften Eintrag bezeichnet und entspricht einem im Schema definierten Attribut. Ein Eigenschaften Eintrag kann einen oder mehrere Eigenschaftswerte aufweisen. Ein Satz von Eigenschaften Einträgen wird als Eigenschaften Liste organisiert.

Die [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle verwaltet die Eigenschafts Liste eines ADSI-Objekts. Die [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) -Schnittstelle führt diesen Vorgang für einen Eigenschafts Eintrag aus. Ebenso stellt die [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) -Schnittstelle einen oder mehrere Eigenschaftswerte dar. Sie bieten einen Mechanismus, mit dem Benutzer folgende Aktionen ausführen können:

-   Arbeiten Sie direkt mit dem Eigenschaften Cache.
-   Arbeiten Sie mit Verzeichnissen, die keine Schemas enthalten, wie z. b. einen LDAP-Server der Version 2.

Die [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* -Schnittstellen arbeiten ausschließlich im Eigenschaften Cache und versuchen nicht, mit dem Server zusammenzuarbeiten, um die Daten im permanenten Speicher abzurufen oder zu ändern. Diese Schnittstellen werden daher nur zum Überprüfen und Bearbeiten von Eigenschaften im Client Cache verwendet. Vor der Verwendung dieser Schnittstellen müssen Sie die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode oder die [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode explizit aufrufen, um die Objekteigenschaften in den Cache zu laden, wenn der Cache nicht initialisiert wurde. Nachdem Sie die Methoden dieser Schnittstellen aufgerufen haben, müssen Sie [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufrufen, um die Änderungen im zugrunde liegenden Verzeichnis Speicher beizubehalten.

Weitere Informationen und ein Codebeispiel, mit dem diese Schnittstellen implementiert werden können, finden Sie unter [Beispielcode für die Verwendung von iadsproperty-Schnittstellen für den Zugriff auf den Eigenschaften Cache](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).

 

 




