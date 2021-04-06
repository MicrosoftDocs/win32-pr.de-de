---
title: Verwenden der IDirectoryObject-Schnittstelle
description: Wenn Sie in C oder C++ einen ADSI-Client erstellen, der eine frühe Bindung verwendet, verfügen Sie über eine größere Anzahl von ADSI-Datentypen, die für den Client verwendet werden können, wenn die IDirectoryObject-Schnittstelle anstelle der IADs-Schnittstelle aufgerufen wird.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, using
- ADSI ADSI, using, mithilfe der IDirectoryObject-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707356"
---
# <a name="using-the-idirectoryobject-interface"></a>Verwenden der IDirectoryObject-Schnittstelle

Wenn Sie in C oder C++ einen ADSI-Client erstellen, der eine frühe Bindung verwendet, verfügen Sie über eine größere Anzahl von ADSI-Datentypen, die für den Client verwendet werden können, wenn die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle anstelle der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle aufgerufen wird. Die **IDirectoryObject** -Schnittstelle stellt Methoden bereit, um eine Teilmenge der Wartungs Eigenschaften eines Objekts und den Zugriff auf seine Attribute zu unterstützen. Die folgende Abbildung zeigt die Beziehungen zwischen den Datenstrukturen.

![IDirectoryObject-Schnittstellen-Datenstrukturen](images/ds2dso.png)

In der obigen Abbildung werden in der Struktur [**ADS \_ Objekt \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_object_info) Eigenschaften definiert, die das Objekt nach dem Distinguished Name, dem relativen Distinguished Name, by Container (parameterdn), dem Objekttyp (classdn) und der Schema Definition (schemadn) identifizieren. Der Attribut Deskriptor [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) besteht aus einem Namen, einem Datentyp, einem Array von Datenwerten, das in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)angezeigt wird, und einem Flag, das den zugrunde liegenden Verzeichnisdienst anweist, bestimmte Vorgänge für die in [ADS \_ attr- \_ \* Konstanten](adsi-constants.md)beschriebenen Attribute auszuführen. Zu den Datentypen für diese Attribute gehören die erweiterten ADSI-Syntax Typen, die in [**adstyetenum**](/windows/win32/api/iads/ne-iads-adstypeenum)ausführlich erläutert werden.

 

 




