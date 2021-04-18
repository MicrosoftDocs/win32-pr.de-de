---
title: Objekte und Eigenschaften
description: Die Eigenschaften eines Objekts in SDO werden durch die Eigenschaften des Objekts und die diesem Eigenschaften zugeordneten Werte bestimmt.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338276"
---
# <a name="objects-and-properties"></a>Objekte und Eigenschaften

Die Eigenschaften eines Objekts in SDO werden durch die Eigenschaften des Objekts und die diesem Eigenschaften zugeordneten Werte bestimmt. Im Gegensatz zu einigen anderen Objekt Modellen verfügen SDO-Objekte selbst über keine Methoden. Allerdings machen SDO-Objekte com-Schnittstellen verfügbar, die Methoden bereitstellen.

Objekte in SDO machen die [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle verfügbar, die Methoden zum Bearbeiten der Objekteigenschaften bereitstellt. Um auf die Eigenschaften des Objekts zuzugreifen, rufen Sie eine **isdo** -Schnittstelle für das Objekt ab, und verwenden Sie die Methoden [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) und [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) Interface, um Werte für die Eigenschaften abzurufen und festzulegen. Das Thema [Abrufen eines Benutzers SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) enthält Beispielcode, der das Abrufen der **isdo** -Schnittstelle für ein Benutzerobjekt veranschaulicht.

Nachdem Sie die Eigenschaften eines Objekts geändert haben, verwenden Sie die [**isdo:: apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) -Methode, um die Änderungen in den persistenten Speicher für das Objekt zu schreiben. Sie können Änderungen, die an den Eigenschaften eines Objekts vorgenommen wurden, Abbrechen, bevor Sie **isdo:: apply** aufrufen, indem Sie die [**isdo:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) -Methode aufrufen. Diese Methode stellt die Werte der Eigenschaften eines Objekts aus dem permanenten Speicher wieder her.

In der folgenden Tabelle sind die Enumerationstypen aufgeführt, die die Eigenschaften einiger der Objekte in SDO auflisten.



| Object                                 | Enumerationstyp                                       |
|----------------------------------------|--------------------------------------------------------|
| Alle SDO-Objekte                        | [**Iascommonproperties**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| User-Objekt                            | [**Eigenschaften**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Dienst Objekt (Netzwerk Richtlinien Server) | [**Iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Microsoft RADIUS-Protokoll Objekt       | [**Radiusproperties**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.

 

## <a name="collections"></a>Sammlungen

Objekte werden häufig in Auflistungen gruppiert. Die SDO-API bietet über die [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) -Auflistungs Schnittstelle Funktionen zum Auflisten der Objekte in einer Auflistung und zum Hinzufügen und Löschen von Objekten aus einer Auflistung.

Der Zugriff auf eine Auflistung wird durch Abrufen einer Auflistungs Eigenschaft für das Objekt abgerufen, das die Auflistung enthält. Weitere Informationen finden Sie im Abschnitt [Objektmodell Hierarchie](/windows/desktop/Nps/sdo-object-model-hierarchy).

Der Datentyp für alle Eigenschaften, die Auflistungen entsprechen, ist VT \_ Dispatch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDO-Objektmodell Hierarchie](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Unterstützte SDO-Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 