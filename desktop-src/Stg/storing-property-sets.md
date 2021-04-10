---
title: Speichern von Eigenschafts Sätzen
description: Anwendungen können einige der Zustandsdaten Ihrer Dokumente verfügbar machen, damit andere Anwendungen diese Daten finden und lesen können.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- Speichern von Eigenschaften Sätzen strukturierter Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60710b84b52fcc709f8ba3ad1e930d6f5a50a4cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855596"
---
# <a name="storing-property-sets"></a>Speichern von Eigenschafts Sätzen

Anwendungen können einige der Zustandsdaten Ihrer Dokumente verfügbar machen, damit andere Anwendungen diese Daten finden und lesen können. Einige Beispiele sind ein Eigenschaften Satz, der den Autor, den Titel und die Schlüsselwörter eines Dokuments beschreibt, das mit einem Textverarbeitungs Tool erstellt wurde, oder die Liste der in einem Dokument verwendeten Schriftarten. Diese Funktion ist nicht auf Dokumente beschränkt. Sie kann auch für eingebettete Objekte verwendet werden. Im Allgemeinen sollte der Zugriff auf Eigenschaften Sätze über die Schnittstellen [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) erfolgen, aber in diesem Abschnitt wird die zuvor empfohlene Vorgehensweise beschrieben.

> [!Note]  
> Wenn Sie einen internen Eigenschaften Satz für Ihre Anwendung speichern, sollten Sie die folgenden Richtlinien möglicherweise nicht verwenden. Befolgen Sie diese Richtlinien, um die Eigenschaften für andere Anwendungen verfügbar zu machen.

 

**So speichern Sie einen Eigenschaften Satz in einer Verbund Datei**

1.  Erstellen Sie eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -oder [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Instanz auf derselben Ebene der Speicherstruktur wie Ihre Datenströme. Befolgen Sie den Namen Ihrer **IStorage** -oder **IStream** -Instanz mit " \\ 005". Datenstrom-und Speicher Namen, die mit 0x05 beginnen, sind für allgemeine Eigenschaften Sätze reserviert, die von Anwendungen gemeinsam verwendet werden können. Außerdem sind Datenströme, die mit diesem Wert beginnen, auf 256 KB beschränkt. Die Namen können entweder aus veröffentlichten Namen und Formaten ausgewählt werden, oder indem Sie die Eigenschaft Set a fmtid zuweisen und den Namen von der fmtid gemäß den in den [Benennungs Konventionen für Speicher Objekte](storage-object-naming-conventions.md)beschriebenen Konventionen ableiten.
2.  Ein Eigenschaften Satz kann in einer einzelnen [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Instanz oder in einer [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Instanz gespeichert werden, die mehrere Streams und Speicher enthält. Bei einer **IStorage** -Instanz ist der enthaltene Stream mit dem Namen "Content" der primäre Stream mit Eigenschafts Werten, wobei einige Werte Namen anderer Streams oder Speicher Instanzen im Speicher für diesen Eigenschaften Satz sein können.
3.  Geben Sie die CLSID der Objektklasse an, die den programmgesteuerten Zugriff auf die Eigenschaftswerte anzeigen oder bereitstellen kann. Wenn keine solche Klasse vorhanden ist, sollte die CLSID auf den Format Bezeichner des Eigenschaften Satzes festgelegt werden. Legen Sie für einen Eigenschaften Satz, der eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Instanz verwendet, entweder die CLSID der **IStorage** -Instanz auf die gleiche fest, die im Inhaltsstream gespeichert ist, oder auf **CLSID \_ null**. der Wert in einer neu erstellten **IStorage** -Instanz.
4.  Sie haben die Möglichkeit, anzeigbare Namen anzugeben, die den Inhalt des Wörterbuchs bilden.

Einige Anwendungen können nur Implementierungen von Eigenschafts Sätzen lesen, die als [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Instanzen gespeichert sind. Anwendungen sollten so geschrieben werden, dass ein Eigenschaften Satz in einer [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -oder **IStream** -Instanz gespeichert werden kann, es sei denn, die Definition der Eigenschaften Menge ist anderweitig angegeben. Beispielsweise gibt die Eigenschaft Festlegung der Zusammenfassungs Informationen an, dass Sie nur in einer benannten **IStream** -Instanz gespeichert werden kann. Wenn Sie nach einem Eigenschaften Satz suchen und nicht wissen, ob es sich um einen Speicher-oder Datenstrom handelt, suchen Sie zuerst nach einer **IStream** -Instanz mit dem Namen der Eigenschaft. Wenn dies nicht möglich ist, suchen Sie nach einer **IStorage** -Instanz.

Um das Speichern von Eigenschafts Sätzen in einer [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Implementierung besser zu verstehen, stellen Sie sich vor, dass es eine Klasse von Anwendungen gibt, die Informationen zu Tieren Zuerst wird eine CLSID (CLSID \_ animalapp) für diese Gruppe von Anwendungen definiert, sodass Sie angeben können, dass Sie Eigenschafts Sätze verstehen, die tierische Informationen (**fmtid \_ animalinfo**) enthalten, und andere, die medizinische Informationen (**fmtid \_ medicalinfo**) enthalten.

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

Beachten Sie, dass die CLSID der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle und beide Eigenschafts Sätze **CLSID \_ animalapp** sind. Dies identifiziert alle Anwendungen, die den programmgesteuerten Zugriff auf diese Eigenschaften Sätze anzeigen und/oder bereitstellen können. Jede Anwendung kann die Daten in den Eigenschaften Sätzen (dem Punkt hinter Eigenschafts Sätzen) lesen, aber nur Anwendungen, die mit dem Klassen Bezeichner der CLSID \_ animalapp identifiziert werden, können die Bedeutung der Daten in den Eigenschaften Sätzen verstehen.

 

 




