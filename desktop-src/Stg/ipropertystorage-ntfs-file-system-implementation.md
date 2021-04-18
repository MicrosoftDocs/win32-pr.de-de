---
title: IPropertyStorage-NTFS-Datei System Implementierung
description: Die NTFS-Version 5,0 bietet eine Implementierung der IPropertyStorage-Schnittstelle für Dateien auf einem NTFS-Volume, wenn die Dateien keine Verbund Dateien sind.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage-Schnittstellen-STG, Implementierungen, NTFS-Dateisystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340917"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage-NTFS-Datei System Implementierung

Die NTFS-Version 5,0 bietet eine Implementierung der [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für Dateien auf einem NTFS-Volume, wenn die Dateien keine Verbund Dateien sind.

**So erhalten Sie einen Zeiger auf die NTFS-Dateisystem Implementierung von IPropertySetStorage**

1.  Rufen Sie [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) mithilfe der NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)auf.
2.  Aufrufen von [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) mithilfe der NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Verwenden Sie [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , um Eigenschaften innerhalb eines einzelnen Eigenschaften Satzes zu verwalten. Die Methoden unterstützen das Lesen, schreiben und Löschen von Eigenschaften und die optionalen Zeichen folgen Namen, die Eigenschafts Bezeichnernamen zugeordnet werden können. Eine andere Methode ermöglicht es Ihnen, Zeiten festzulegen, die dem Eigenschaften Speicher zugeordnet sind, und ein anderes ermöglicht die Zuweisung einer CLSID, die zum Zuordnen von anderem Code, z. b. Benutzeroberflächen Code, mit dem Eigenschaften Satz verwendet wird. Der Aufruf der [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) -Methode liefert einen Zeiger auf die NTFS-Implementierung von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), mit der Sie die Eigenschaften in der Menge auflisten können.

## <a name="remarks"></a>Bemerkungen

Die NTFS-Implementierung bietet im wesentlichen dieselben Funktionen wie die Implementierung der Verbund Datei. Weitere Informationen finden Sie unter [IPropertyStorage-Verbund Datei Implementierung](ipropertystorage-compound-file-implementation.md).

Da NTFS ein robustes Dateisystem ist, bleibt ein NTFS-Eigenschaften Satz nie in einem falschen Zustand. Wenn der Inhalt eines NTFS- [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) in die zugrunde liegende NTFS-Datei geleert wird, werden entweder alle oder keine der Zustände als atomarer Vorgang in die Datei geschrieben, auch wenn während des Vorgangs ein Fehler auftritt, z. b. eine ungewöhnliche Prozess Beendigung. Um ein ähnliches Verhalten mit der Implementierung der Verbund Datei zu erzielen, muss die übergeordnete [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle im transaktiven Modus geöffnet werden.

Diese Robustheit ist nur möglich, wenn auf eine NTFS-Eigenschaft zugegriffen wird, die auf einem NTFS 5,0-Volume festgelegt ist. Es ist möglich, auf NTFS-Eigenschaften Sätze in früheren Versionen von NTFS zuzugreifen (z. b. auf einem Computer unter Windows NT oder Windows 2000, der auf die Eigenschaften Sätze auf einem Dateiserver Computer unter Windows NT 4,0 zugreift), während ein unerwarteter Fehler nicht gewährleistet ist, dass Sie den richtigen Zustand aufweisen.

Obwohl die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) keine Unterstützung für Transaktionen bietet, unterstützt Sie die NTFS-Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Das heißt, dass **STGM \_ transaktive** im *grfMode* -Parameter für die [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -und [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode von **IPropertySetStorage** angegeben werden kann. Wie bei der Implementierung der Verbund Datei ist der transaktive Modus nur für nicht einfache Eigenschafts Speicher möglich (bei Angabe von **propsetflag \_ nicht einfache** im *grfFlags* -Parameter).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage-NTFS-Datei System Implementierung](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 