---
description: Um Namenskonflikte zwischen Eigenschaften zu verhindern, die von unterschiedlichen Objekten erstellt wurden, verwendet der Shared Property Manager (SPM) freigegebene Eigenschaften Gruppen.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Freigegebene Eigenschaften Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761112"
---
# <a name="shared-property-groups"></a>Freigegebene Eigenschaften Gruppen

Um Namenskonflikte zwischen Eigenschaften zu verhindern, die von unterschiedlichen Objekten erstellt wurden, verwendet der Shared Property Manager (SPM) freigegebene Eigenschaften Gruppen. Eine freigegebene Eigenschaften Gruppe ist einfach ein Namespace für einen Satz von freigegebenen Eigenschaften. Jede Eigenschaft in einer freigegebenen Eigenschaften Gruppe besteht aus einem Namen, einem Wert und einer Position in der Gruppe der freigegebenen Eigenschaften. Der Name oder die Position kann verwendet werden, um den Eigenschafts Wert abzurufen. Sie können auf freigegebene Eigenschaften Gruppen zugreifen und diese über den freigegebenen Eigenschaften Gruppen-Manager erstellen.

Das SPM-Objektmodell ist in der folgenden Abbildung dargestellt.

![Diagramm, das das SPM-Objektmodell zeigt: ISharedPropertyGroupManager, ISharedPropertyGroup und ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

Die folgenden Schnittstellen sind im freigegebenen Eigenschaften-Manager aufgeführt:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) wird verwendet, um freigegebene Eigenschaften Gruppen zu erstellen und um Zugriff auf vorhandene freigegebene Eigenschaften Gruppen zu erhalten. Sie können auf die **ISharedPropertyGroupManager** -Schnittstelle zugreifen, indem Sie eine Instanz des [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) -Objekts erstellen, indem Sie entweder [**IObjectContext:: kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) oder [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)verwenden.

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) wird verwendet, um die freigegebenen Eigenschaften in einer freigegebenen Eigenschaften Gruppe zu erstellen und darauf zuzugreifen. Sie können auf die **ISharedPropertyGroup** -Schnittstelle zugreifen, indem Sie ein [**SharedPropertyGroup**](sharedpropertygroup.md) -Objekt mit der [**ISharedPropertyGroupManager:: kreatepropertygroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) -Methode erstellen. Wie bei jedem COM-Objekt müssen Sie ein **SharedPropertyGroup** -Objekt freigeben, wenn Sie es nicht mehr benötigen.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) wird verwendet, um den Wert einer freigegebenen Eigenschaft festzulegen oder abzurufen. Eine freigegebene Eigenschaft kann jeden beliebigen Datentyp enthalten, der durch eine Variante dargestellt werden kann. Sie können auf die **ISharedProperty** -Schnittstelle zugreifen, indem Sie ein [**SharedProperty**](sharedproperty.md) -Objekt mit der [**ISharedPropertyGroup:: kreateproperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) -Methode oder der [**ISharedPropertyGroup:: deatepropertybyposition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) -Methode erstellen. Ein **SharedProperty** -Objekt kann nur innerhalb eines [**SharedPropertyGroup**](sharedpropertygroup.md) -Objekts erstellt oder darauf zugegriffen werden. Auch hier müssen Sie ein **SharedProperty** -Objekt freigeben, wenn Sie es nicht mehr benötigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gemeinsam genutztes com+-Eigenschaften-Manager](com--shared-property-manager.md)
</dt> </dl>

 

 
