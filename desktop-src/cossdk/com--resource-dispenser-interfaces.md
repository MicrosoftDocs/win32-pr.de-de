---
description: COM+-Ressourcenausgabeschnittstellen
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: COM+-Ressourcenausgabeschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7fa011681defaddc160e835c7caeb6719054f5e4397903a1716ae76f81c7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991520"
---
# <a name="com-resource-dispenser-interfaces"></a>COM+-Ressourcenausgabeschnittstellen

Anwendungskomponenten verwenden Ressourcenspender für den Zugriff auf freigegebene Informationen. Die in der folgenden Tabelle beschriebenen Schnittstellen enthalten ausführliche Referenzinformationen für Entwickler von Ressourcensendern.



| Schnittstellen                                                | Beschreibung                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | Diese Schnittstelle wird vom Besitzer des Ressourcensenders aufgerufen, um eine Ressource zu erstellen, zu eintragungen, zu bewerten und zu zerstören.<br/> |
| [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | Ressourcenspender verwenden diese Schnittstelle, um eine Verbindung mit dem Versender-Manager herzustellen.<br/>                                    |
| [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | Diese Schnittstelle wird verwendet, um Ressourcen vorzubereiten und zu verarbeiten.<br/>                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DES COM+-Ressourcensenders](com--resource-dispenser-concepts.md)
</dt> <dt>

[In COM+-Ressourcenspenderschnittstellen verwendete Typen](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




