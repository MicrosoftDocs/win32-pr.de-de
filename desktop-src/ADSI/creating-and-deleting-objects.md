---
title: Erstellen und Löschen von Objekten
description: Mit ADSI werden Objekte mithilfe der IADsContainer-Schnittstelle oder der IDirectoryObject-Schnittstelle erstellt und gelöscht.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Erstellen und Löschen von Objekten ADSI
- ADSI, erstellen und Löschen von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4730c4cc6a95ad37bfd3953474d3d488fcf05abb
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474236"
---
# <a name="creating-and-deleting-objects"></a>Erstellen und Löschen von Objekten

Mit ADSI werden Objekte mithilfe der [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle oder der [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle erstellt und gelöscht.

## <a name="creating-an-object-with-iadscontainer"></a>Erstellen eines Objekts mit IADsContainer

**So erstellen Sie ein Objekt mit der IADsContainer-Schnittstelle**

1.  Binden Sie an den Container, der das zu erstellende Objekt enthalten soll, und rufen Sie die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle ab.
2.  Verwenden Sie die [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) -Methode, um ein neues-Objekt im Container zu erstellen.
3.  Legen Sie die Werte für alle erforderlichen Attribute für das-Objekt mithilfe der [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -oder [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode fest. Die zum Erstellen eines Objekts erforderlichen Attribute hängen vom Verzeichnisdienst und dem Objekttyp ab, der erstellt wird. Weitere Informationen zum Erstellen von Active Directory Objekten finden Sie unter [Erstellen und Löschen von Active Directory Objekten](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Legen Sie die Werte für alle gewünschten optionalen Attribute für das-Objekt mithilfe der [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -oder [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode fest.
5.  Ruft die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode auf, um ein Commit für das Objekt und seine Attribute durchzusetzen. Das neue-Objekt wird tatsächlich nicht im zugrunde liegenden Verzeichnisdienst erstellt, bis die **IADs. SetInfo** -Methode aufgerufen wird, um ein Commit für die Attribute durchzusetzen.

## <a name="creating-an-object-with-idirectoryobject"></a>Erstellen eines Objekts mit IDirectoryObject

**So erstellen Sie ein Objekt mit der IDirectoryObject-Schnittstelle**

1.  Binden Sie an den Container, der das zu erstellende Objekt enthalten soll, und rufen Sie die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle ab.
2.  Ordnen Sie ein Array von [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Strukturen zu, das eine Struktur für jedes Attribut enthält, das beim Erstellen des Objekts festgelegt werden soll.
3.  Füllen Sie eine [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur für jedes erforderliche Attribut für das Objekt aus. Die zum Erstellen eines Objekts erforderlichen Attribute hängen vom Verzeichnisdienst und dem Objekttyp ab, der erstellt wird. Weitere Informationen zum Erstellen von Active Directory Objekten finden Sie unter [Erstellen und Löschen von Active Directory Objekten](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Füllen Sie eine [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur für jedes optionale Attribut für das Objekt aus.
5.  Verwenden Sie die [**IDirectoryObject:: kreatedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) -Methode, um das Objekt im Container zu erstellen. Diese Methode führt auch ein Commit für das-Objekt an den zugrunde liegenden Verzeichnisdienst aus. Wenn das [**ADS- \_ \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Array nicht alle erforderlichen Attribute für das-Objekt enthält, schlägt **IDirectoryObject:: deedsobject** fehl.

## <a name="deleting-an-object"></a>Löschen eines Objekts

Zum Löschen eines Objekts verwenden Sie die [**IADsContainer::D Elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) -Methode oder die [**IDirectoryObject::D eletedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) -Methode. Diese Methoden können nicht ausgeführt werden, wenn das gelöschte Objekt untergeordnete Objekte enthält. Verwenden Sie die [**iadsdeleteops::D eleteobject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) -Methode, um einen Container und alle untergeordneten Objekte des Containers zu löschen.

Was mit einem gelöschten Objekt passiert, hängt vom zugrunde liegenden Verzeichnisdienst ab. Weitere Informationen zum Löschen von Active Directory Objekten finden Sie unter [Erstellen und Löschen von Active Directory Objekten](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).

 

 