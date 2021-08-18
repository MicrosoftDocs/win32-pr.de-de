---
title: Abrufen einer Link-ID
description: Ab Windows Server 2003 ist es nicht mehr erforderlich, eine linkID von Microsoft an fordern. es gibt einen Prozess zum automatischen Generieren einer linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Abrufen einer Link-ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1800448e8cc665e0a28a88800a592e33d7b6ee5a766743d8a681a121c5ad02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025558"
---
# <a name="obtaining-a-link-id"></a>Abrufen einer Link-ID

Ab Windows Server 2003 ist es nicht mehr erforderlich, eine [**linkID**](/windows/desktop/ADSchema/a-linkid) von Microsoft an fordern. es gibt einen Prozess zum automatischen Generieren einer **linkID**. Das System generiert automatisch eine Link-ID für ein neues verknüpftes Attribut, wenn das **linkID-Attribut** des Attributs auf 1.2.840.113556.1.2.50 festgelegt ist. Ein Rücklink für diesen Vorwärtslink wird erstellt, indem die **linkID** auf [**die attributeID**](/windows/desktop/ADSchema/a-attributeid) oder [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) des Forward-Links festlegen. Der Schemacache muss nach dem Erstellen des Forwardlinks und vor dem Erstellen des Backlinks erneut geladen werden. Andernfalls werden **attributeId** oder **ldapDisplayName** des Forwardlinks nicht gefunden, wenn der Backlink erstellt wird. Der Schemacache wird bei Bedarf, einige Minuten nach einer Schemaänderung oder beim Neustart des Domänencontrollers erneut geladen. Erstellen Sie alle Vorwärtslinks, laden Sie den Schemacache neu, und erstellen Sie dann alle Backlinks.

Wenn Sie beispielsweise die neuen Attribute **myForwardLinkAttr** und **myBackLinkAttr** erstellt haben und diese verknüpfen möchten:

> [!Note]  
> Die OIDs in diesem Beispiel werden konverkriert. Anweisungen [zum Abrufen von](obtaining-an-object-identifier-from-microsoft.md) OIDs für neue Attribute finden Sie unter Abrufen eines Objektbezeichners von Microsoft.

 

1.  Legen Sie diese Attribute für das Attribut fest, das als Vorwärtslink verwendet werden soll:
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Laden Sie das Schema erneut.
3.  Legen Sie diese Attribute für das Attribut fest, das als Backlink verwendet werden soll:
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verknüpfte Attribute](linked-attributes.md)
</dt> <dt>

[Erweitern des Schemas](how-to-extend-the-schema.md)
</dt> </dl>

 

 