---
title: Access Control-und Schreibvorgänge
description: Eigenschafts Änderungen schlagen fehl, wenn der Aufrufer nicht über ausreichende Rechte verfügt.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Access Control-und Writer-Vorgänge AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858113"
---
# <a name="access-control-and-write-operations"></a>Access Control-und Schreibvorgänge

Eigenschafts Änderungen schlagen fehl, wenn der Aufrufer nicht über ausreichende Rechte verfügt. Bei Schreibvorgängen, bei denen Änderungen an mehreren Eigenschaften in Batches ausgeführt werden, schlägt der gesamte Vorgang fehl, wenn der Aufrufer nicht über die erforderlichen Rechte für eine einzelne der geänderten Eigenschaften verfügt. Beispielsweise können Sie mehrere [**IADs erstellen::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Aufrufe, um mehrere Eigenschaften für ein Objekt festzulegen. Wenn Sie jedoch " [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) " aufrufen, um die neuen Daten aus dem lokalen Cache in das Verzeichnis zu schreiben, schlägt " **stinfo** " fehl, wenn der Aufrufer keinen Schreibzugriff auf alle geänderten Eigenschaften hat. Ebenso kann die [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) -Methode keine Eigenschaften festlegen, wenn der Aufrufer keinen Zugriff auf alle Eigenschaften hat, die festgelegt werden. Daher sollten Sie mehrere Änderungs Vorgänge nur dann in Batches Verpacken, wenn Sie wissen, dass alle Änderungen erfolgreich sind. Um die Attribute eines Verzeichnis Objekts zu ermitteln, das der Aufrufer ändern kann, lesen Sie das Attribut " **attributedattributeseffective** " des Objekts.

Wenn der Aufrufer nicht über ausreichende Rechte verfügt, um eine Eigenschaft zu ändern, können die folgenden Rückgabecodes zurückgegeben werden:

e \_ ADS- \_ Eigenschaft \_ nicht \_ festgelegt e \_ ADS- \_ Eigenschaft \_ nicht \_ geändert

 

 