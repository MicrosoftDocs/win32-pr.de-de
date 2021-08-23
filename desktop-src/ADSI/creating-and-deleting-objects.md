---
title: Erstellen und Löschen von Objekten
description: Mit ADSI werden Objekte entweder über die IADsContainer- oder die IDirectoryObject-Schnittstelle erstellt und gelöscht.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Erstellen und Löschen von Objekten ADSI
- ADSI, Erstellen und Löschen von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bf2e351fb9bae919e8c40b0682b456b793f2e4419a66c64242791fad1d6cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023648"
---
# <a name="creating-and-deleting-objects"></a>Erstellen und Löschen von Objekten

Mit ADSI werden Objekte entweder über die [**IADsContainer-**](/windows/desktop/api/Iads/nn-iads-iadscontainer) oder [**die IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) erstellt und gelöscht.

## <a name="creating-an-object-with-iadscontainer"></a>Erstellen eines Objekts mit IADsContainer

**So erstellen Sie ein Objekt mit der IADsContainer-Schnittstelle**

1.  Binden Sie an den Container, der das zu erstellende Objekt enthält, und rufen Sie die [**IADsContainer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ab.
2.  Verwenden Sie die [**IADsContainer.Create-Methode,**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) um ein neues -Objekt im Container zu erstellen.
3.  Legen Sie die Werte für alle erforderlichen Attribute für das Objekt mithilfe der [**IADs.Put-**](/windows/desktop/api/Iads/nf-iads-iads-put) oder [**IADs.PutEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-putex) fest. Welche Attribute zum Erstellen eines Objekts erforderlich sind, hängt vom Verzeichnisdienst und vom Typ des erstellten Objekts ab. Weitere Informationen zum Erstellen von Active Directory-Objekten finden Sie unter [Erstellen und Löschen von Active Directory-Objekten.](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)
4.  Legen Sie die Werte für alle gewünschten optionalen Attribute für das Objekt mithilfe der [**IADs.Put-**](/windows/desktop/api/Iads/nf-iads-iads-put) oder [**IADs.PutEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-putex) fest.
5.  Rufen Sie die [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) auf, um das Objekt und seine Attribute zu committen. Das neue Objekt wird erst dann im zugrunde liegenden Verzeichnisdienst erstellt, wenn die **IADs.SetInfo-Methode** aufgerufen wird, um die Attribute zu committen.

## <a name="creating-an-object-with-idirectoryobject"></a>Erstellen eines Objekts mit IDirectoryObject

**So erstellen Sie ein Objekt mit der IDirectoryObject-Schnittstelle**

1.  Binden Sie an den Container, der das zu erstellende Objekt enthält, und rufen Sie die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ab.
2.  Ordnen Sie ein Array von [**ADS \_ ATTR \_ INFO-Strukturen**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) zu, das eine Struktur für jedes Attribut enthält, das beim Erstellen des Objekts festgelegt werden soll.
3.  Füllen Sie eine [**ADS \_ ATTR \_ INFO-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) für jedes erforderliche Attribut für das Objekt aus. Welche Attribute zum Erstellen eines Objekts erforderlich sind, hängt vom Verzeichnisdienst und vom Typ des erstellten Objekts ab. Weitere Informationen zum Erstellen von Active Directory-Objekten finden Sie unter [Erstellen und Löschen von Active Directory-Objekten.](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)
4.  Geben Sie für jedes optionale Attribut für das Objekt eine [**ADS \_ ATTR \_ INFO-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) ein.
5.  Verwenden Sie die [**IDirectoryObject::CreateDSObject-Methode,**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) um das Objekt im Container zu erstellen. Diese Methode committet auch das -Objekt an den zugrunde liegenden Verzeichnisdienst. Wenn das [**ADS \_ ATTR \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) nicht alle erforderlichen Attribute für das Objekt enthält, schlägt **IDirectoryObject::CreateDSObject** fehl.

## <a name="deleting-an-object"></a>Löschen eines Objekts

Verwenden Sie zum Löschen eines Objekts die [**Methode IADsContainer::D elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) oder [**IDirectoryObject::D eleteDSObject.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) Diese Methoden schlagen fehl, wenn das gelöschte Objekt untergeordnete Objekte enthält. Verwenden Sie die [**IADsDeleteOps::D eleteObject-Methode,**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) um einen Container und alle untergeordneten Objekte des Containers zu löschen.

Was mit einem gelöschten Objekt geschieht, hängt vom zugrunde liegenden Verzeichnisdienst ab. Weitere Informationen zum Löschen von Active Directory-Objekten finden Sie unter [Erstellen und Löschen von Active Directory-Objekten.](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)

 

 