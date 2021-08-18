---
title: Verwenden der IDirectoryObject-Schnittstelle
description: Wenn Sie einen ADSI-Client in C oder C++ erstellen, der eine frühe Bindung verwendet, stehen Ihnen eine größere Bandbreite von ADSI-Datentypen zur Verfügung, die für Ihren Client verwendet werden können, wenn er die IDirectoryObject-Schnittstelle anstelle der IADs-Schnittstelle aufruft.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI mit
- ADSI ADSI mithilfe der IDirectoryObject-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d085344e5d2d1afe975dd347ff9e9cf4cdad99c1177819e0094b7a83f2219fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023082"
---
# <a name="using-the-idirectoryobject-interface"></a>Verwenden der IDirectoryObject-Schnittstelle

Wenn Sie einen ADSI-Client in C oder C++ erstellen, der eine frühe Bindung verwendet, stehen Ihnen eine größere Bandbreite von ADSI-Datentypen zur Verfügung, die für Ihren Client verwendet werden können, wenn er die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) anstelle der [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) aufruft. Die **IDirectoryObject-Schnittstelle** stellt Methoden bereit, um eine Teilmenge der Wartungseigenschaften eines Objekts zu unterstützen und auf seine Attribute zuzugreifen. Die folgende Abbildung zeigt die Beziehungen zwischen den Datenstrukturen.

![Datenstrukturen der idirectoryobject-Schnittstelle](images/ds2dso.png)

In der obigen Abbildung definiert die Struktur [**ADS \_ OBJECT \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) Eigenschaften, die das Objekt anhand des Distinguished Name, des relativen Distinguished Name, des Containers (ParentDN), des Objekttyps (ClassDN) und der Schemadefinition (SchemaDN) identifizieren. Der Attributdeskriptor [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) besteht aus einem Namen, einem Datentyp, einem Array von Datenwerten, die in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)angezeigt werden, und einem Flag, das den zugrunde liegenden Verzeichnisdienst anweist, bestimmte Vorgänge für die In [ADS \_ ATTR-Konstanten \_ \* angegebenen](adsi-constants.md)Attribute auszuführen. Zu den Datentypen für diese Attribute gehören die erweiterten ADSI-Syntaxtypen, die in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)ausführlich beschrieben sind.

 

 




