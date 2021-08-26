---
title: Datenübertragung
description: Datenübertragung
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98e7f546cab245e1f2d2d06036379ea5b28526edcf42aa8a364ea04688db034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993488"
---
# <a name="data-transfer"></a>Datenübertragung

Das Component Object Model (COM) bietet einen Standardmechanismus zum Übertragen von Daten zwischen Anwendungen. Dieser Mechanismus ist das *Datenobjekt,* bei dem es sich einfach um ein beliebiges COM-Objekt handelt, das die [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) implementiert. Einige Datenobjekte, z. B. ein text-Element, das in die Zwischenablage kopiert wird, haben **IDataObject** als einzige Schnittstelle. Andere, z. B. zusammengesetzte Dokumentobjekte, machen mehrere Schnittstellen verfügbar, von denen **IDataObject einfach** eine ist. Datenobjekte sind für die Arbeit von Verbunddokumenten von grundlegender Bedeutung, obwohl sie auch außerhalb dieser OLE-Technologie weit verbreitet sind.

Durch den Austausch von Zeigern auf ein Datenobjekt können Anbieter und Verbraucher von Daten Datenübertragungen auf einheitliche Weise verwalten, unabhängig vom Format der Daten, dem Typ des Mediums, das zum Übertragen der Daten verwendet wird, oder dem Zielgerät, auf dem sie gerendert werden sollen. You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). Wenn dies erfolgt ist, ist die Menge an Code, die erforderlich ist, um die spezielle Semantik der einzelnen Protokolle zu unterstützen, minimal.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Datenübertragungsschnittstellen](data-transfer-interfaces.md)
-   [Datenformate und Übertragungsmedien](data-formats-and-transfer-media.md)
-   [Drag &amp; Drop](drag-and-drop.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbunddokumente](compound-documents.md)
</dt> </dl>

 

 




