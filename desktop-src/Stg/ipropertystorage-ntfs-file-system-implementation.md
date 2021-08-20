---
title: IPropertyStorage-NTFS-Dateisystemimplementierung
description: Die NTFS-Version 5.0 stellt eine Implementierung der IPropertyStorage-Schnittstelle für Dateien auf einem NTFS-Volume bereit, wenn es sich bei den Dateien nicht um Verbunddateien handelt.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd Stg , Implementierungen, NTFS-Dateisystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91db3242761867eb3ec9f9cf744e6b20db3ac1ef5f0e4fef2ae1c460f182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961269"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage-NTFS-Dateisystemimplementierung

Die NTFS-Version 5.0 stellt eine Implementierung der [**IPropertyStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) für Dateien auf einem NTFS-Volume bereit, wenn es sich bei den Dateien nicht um Verbunddateien handelt.

**So erhalten Sie einen Zeiger auf die NTFS-Dateisystemimplementierung von IPropertySetStorage**

1.  Rufen [**Sie IPropertySetStorage::Create mithilfe**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) der NTFS-Implementierung von [**IPropertySetStorage auf.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
2.  Rufen [**Sie IPropertySetStorage::Open mithilfe**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) der NTFS-Implementierung von [**IPropertySetStorage auf.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

## <a name="when-to-use"></a>Verwendung

Verwenden [**Sie IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) um Eigenschaften innerhalb eines einzelnen Eigenschaftensets zu verwalten. Die zugehörigen Methoden unterstützen das Lesen, Schreiben und Löschen von Eigenschaften und die optionalen Zeichenfolgennamen, die Eigenschaftsbezeichnern zugeordnet werden können. Eine andere Methode ermöglicht ihnen das Festlegen von Zeiten, die dem Eigenschaftenspeicher zugeordnet sind, und eine andere ermöglicht die Zuweisung einer CLSID, die verwendet wird, um anderen Code, z. B. Benutzeroberflächencode, dem Eigenschaftensatz zu zuordnen. Das Aufrufen [**der Enum-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) stellt einen Zeiger auf die NTFS-Implementierung von [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)zur Verfügung, mit der Sie die Eigenschaften in der Gruppe aufzählen können.

## <a name="remarks"></a>Hinweise

Die NTFS-Implementierung bietet im Wesentlichen die gleichen Features wie die Verbunddateiimplementierung. Weitere Informationen finden Sie unter [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).

Da NTFS ein stabiles Dateisystem ist, wird ein NTFS-Eigenschaftensatz nie in einem falschen Zustand befließen. Wenn der Inhalt einer [**NTFS-IPropertyStorage-Datei**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) in die zugrunde liegende NTFS-Datei geleert wird, wird entweder der ganze oder keiner der Status als atomarer Vorgang in die Datei geschrieben, selbst wenn während des Vorgangs ein Fehler vor sich geht, z. B. eine ungewöhnliche Prozessbeendigung. Um ein ähnliches Verhalten mit der Verbunddateiimplementierung zu erzielen, muss die übergeordnete [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) im Transaktionsmodus geöffnet werden.

Diese Stabilitätsstufe ist nur möglich, wenn auf eine NTFS-Eigenschaft, die auf einem NTFS 5.0-Volume festgelegt ist, zu zugreifen. Es ist möglich, auf NTFS-Eigenschaftensätze in früheren Versionen von NTFS zu zugreifen (z. B. auf einem Computer, der unter Windows NT oder Windows 2000 ausgeführt wird und auf die Eigenschaftensätze auf einem Dateiservercomputer unter Windows NT 4.0 zugeht), bei einem unerwarteten Fehler wird jedoch nicht garantiert, dass sie sich in einem richtigen Zustand befinden.

Obwohl die NTFS-Implementierung [**von IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) keine Transaktion unterstützt, wird sie von der NTFS-Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt. Das heißt, **STGM \_ TRANSACTED** kann im *grfMode-Parameter* für die [**Create-**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) und [**Open-Methoden**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) von **IPropertySetStorage angegeben werden.** Wie bei der Verbunddateiimplementierung ist der Transaktionsmodus nur für nicht einfache Eigenschaftenspeicher möglich (Angabe **von PROPSETFLAG \_ NONSIMPLE** im *parameter grfFlags).*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage-NTFS-Dateisystemimplementierung](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 