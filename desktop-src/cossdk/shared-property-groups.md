---
description: Um Namenskonflikte zwischen Eigenschaften zu verhindern, die von verschiedenen Objekten erstellt wurden, verwendet der Freigegebene Eigenschaften-Manager (SHARED Property Manager, SPM) freigegebene Eigenschaftengruppen.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Freigegebene Eigenschaftengruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cda375c09b164e4ed380ba7d89477f2225b5b6004f98299ec9fd9b46f80abee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029215"
---
# <a name="shared-property-groups"></a>Freigegebene Eigenschaftengruppen

Um Namenskonflikte zwischen Eigenschaften zu verhindern, die von verschiedenen Objekten erstellt wurden, verwendet der Freigegebene Eigenschaften-Manager (SHARED Property Manager, SPM) freigegebene Eigenschaftengruppen. Eine freigegebene Eigenschaftengruppe ist einfach ein Namespace für einen Satz freigegebener Eigenschaften. Jede Eigenschaft innerhalb einer freigegebenen Eigenschaftengruppe besteht aus einem Namen, einem Wert und einer Position innerhalb der freigegebenen Eigenschaftengruppe. Der Name oder die Position kann zum Abrufen des Eigenschaftswerts verwendet werden. Sie können über den Gruppen-Manager für freigegebene Eigenschaften auf freigegebene Eigenschaftengruppen zugreifen und diese erstellen.

Das SPM-Objektmodell ist in der folgenden Abbildung dargestellt.

![Diagramm, das das SPM-Objektmodell zeigt: ISharedPropertyGroupManager, ISharedPropertyGroup, zu ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

Es folgen Schnittstellen des freigegebenen Eigenschaften-Managers:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) wird verwendet, um freigegebene Eigenschaftengruppen zu erstellen und Zugriff auf vorhandene freigegebene Eigenschaftengruppen zu erhalten. Sie können auf die **ISharedPropertyGroupManager-Schnittstelle** zugreifen, indem Sie eine Instanz des [**SharedPropertyGroupManager-Objekts**](sharedpropertygroupmanager.md) erstellen, indem Sie entweder [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) oder [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)verwenden.

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) wird verwendet, um die freigegebenen Eigenschaften in einer freigegebenen Eigenschaftengruppe zu erstellen und darauf zuzugreifen. Sie können auf die **ISharedPropertyGroup-Schnittstelle** zugreifen, indem Sie ein [**SharedPropertyGroup-Objekt**](sharedpropertygroup.md) mit der [**ISharedPropertyGroupManager::CreatePropertyGroup-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) erstellen. Wie bei jedem COM-Objekt müssen Sie ein **SharedPropertyGroup-Objekt** freigeben, wenn Sie es nicht mehr verwenden.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) wird verwendet, um den Wert einer freigegebenen Eigenschaft festzulegen oder abzurufen. Eine freigegebene Eigenschaft kann jeden Datentyp enthalten, der durch eine Variante dargestellt werden kann. Sie können auf die **ISharedProperty-Schnittstelle** zugreifen, indem Sie ein [**SharedProperty-Objekt**](sharedproperty.md) mit der [**ISharedPropertyGroup::CreateProperty-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) oder der [**ISharedPropertyGroup::CreatePropertyByPosition-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) erstellen. Ein **SharedProperty-Objekt** kann nur innerhalb eines [**SharedPropertyGroup-Objekts**](sharedpropertygroup.md) erstellt oder darauf zugegriffen werden. Auch hier müssen Sie ein **SharedProperty-Objekt** freigeben, wenn Sie es nicht mehr verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[FREIGEGEBENE COM+-Eigenschaften-Manager](com--shared-property-manager.md)
</dt> </dl>

 

 
