---
title: Eigenschaften Blatt "Drucken"
description: Das Druckeigenschaften Blatt ist eine Standardbenutzer Oberfläche, die es dem Benutzer ermöglicht, die Eigenschaften eines bestimmten Druckauftrags anzugeben.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, allgemeine Dialog Feld Bibliothek
- Benutzereingabe, allgemeine Dialog Feld Bibliothek
- Erfassen von Benutzereingaben, allgemeine Dialog Feld Bibliothek
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Dialogfeld "Eigenschaften Blatt drucken"
- Dialogfeld zum Anpassen des Druckeigenschaften Blatts
- vordefinierte Dialogfelder
- Dialogfelder, Eigenschaften Blatt drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20905f76af290b3978bec828a382604147297998
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039576"
---
# <a name="print-property-sheet"></a>Eigenschaften Blatt "Drucken"

Das **Druck** Eigenschaften Blatt ist eine Standardbenutzer Oberfläche, die es dem Benutzer ermöglicht, die Eigenschaften eines bestimmten Druckauftrags anzugeben. Das Eigenschaften Blatt besteht aus einem Satz von Eigenschaften Seiten, die je nach Drucker oder Anwendung variieren. Für eine Teilmenge der standardmäßigen Windows-Eigenschaften Seiten können einige Druckertreiber spezifische Eigenschaften Seiten hinzufügen, und einige Anwendungen können anwendungsspezifische Eigenschaften Seiten hinzufügen.

Zum Erstellen und Anzeigen eines **Druck** Eigenschaften Blatts initialisieren Sie eine [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur, und übergeben Sie die Struktur an die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion.

Die folgende Abbildung zeigt ein typisches **Druck** Eigenschaften Blatt.

![Drucker-Eigenschaften Blatt](images/printerpropertypagexp.png)

Die meisten Member der [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur sind identisch mit denen der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur. Beschreibungen der Verwendung der allgemeinen Strukturmember für die Interaktion mit den Dialogfeld-Steuerelementen finden Sie unter [Dialogfeld "Drucken](print-dialog-box.md)". Im restlichen Teil dieses Themas werden die Funktionen für **Druck** Eigenschaften Seiten beschrieben, die sich vom Dialogfeld **Drucken** unterscheiden.

Sie können ein **Druck** Eigenschaften Blatt anpassen, indem Sie eine benutzerdefinierte Dialogfeld Vorlage für den unteren Teil der Seite **Allgemein** angeben und zusätzliche Eigenschaften Seiten angeben, die der Seite **Allgemein** folgen. Weitere Informationen finden Sie unter [Anpassen des Druckeigenschaften Blatts](#customizing-the-print-property-sheet).

Sie können ein Rückruf Objekt implementieren, um Benachrichtigungen und Meldungen von der [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion zu empfangen, während das Eigenschaften Blatt angezeigt wird. Anwendungen, die benutzerdefinierte Vorlagen oder zusätzliche Seiten bereitstellen, verwenden das Rückruf Objekt für die Kommunikation mit dem Eigenschaften Blatt. Weitere Informationen finden Sie unter [Callback-Objekt für das Druckeigenschaften Blatt](#callback-object-for-the-print-property-sheet).

Das **Druck** Eigenschaften Blatt bietet Unterstützung für das Angeben mehrerer, nicht zusammenhängender Seitenbereiche, die gedruckt werden sollen. Der **lppageranges** -Member der [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur gibt ein Array von [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) -Strukturen an, in denen jede Struktur einen Seitenbereich angibt.

Das **Druck** Eigenschaften Blatt zeigt ein Optionsfeld für die **aktuelle Seite** als Teil der **Seitenbereichs** Gruppe von Options Feldern an. Um das Optionsfeld für die **aktuelle Seite** zu steuern, verwenden Sie die Flags **PD \_ CurrentPage** und **PD \_ nocurrentpage** im **Flags** -Member der [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Anpassen des Druckeigenschaften Blatts](#customizing-the-print-property-sheet)
-   [Rückruf Objekt für das Druckeigenschaften Blatt](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Anpassen des Druckeigenschaften Blatts

Sie können das **Druck** Eigenschaften Blatt wie folgt anpassen:

-   Geben Sie eine benutzerdefinierte Vorlage für den unteren Teil der Seite **Allgemein** an. Dadurch können Sie zusätzliche Steuerelemente einschließen, die für Ihre Anwendung eindeutig sind. Die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion verwendet anstelle der Standardvorlage Ihre benutzerdefinierte Vorlage.
-   Geben Sie zusätzliche Eigenschaften Seiten an, um der Seite **Allgemein** zu folgen.
-   Geben Sie ein Rückruf Objekt an. Weitere Informationen finden Sie unter [Callback-Objekt für das Druckeigenschaften Blatt](#callback-object-for-the-print-property-sheet).

Der obere Teil der Seite **Allgemein** kann nicht geändert werden. Eigenschaften Seiten, die vom Druckertreiber bereitgestellt werden, können nicht geändert werden.

So geben Sie eine benutzerdefinierte Vorlage für die Seite "Allgemein" an:

1.  Erstellen Sie eine benutzerdefinierte Vorlage für den unteren Teil der Seite **Allgemein** , indem Sie die in der Datei prnsetup. DLG angegebene printdlgexord-Vorlage ändern. In der Regel muss die benutzerdefinierte Vorlage dieselbe Größe aufweisen wie die Standardvorlage. Sie können jedoch die benutzerdefinierte Vorlage vergrößern, wenn Sie das Flag " **PD \_ uselargetemplate** " angeben, um eine größere **Allgemeine** Seite zu erstellen. Die in der standardmäßigen **Druck** Dialogfeld Vorlage verwendeten Steuerelement-IDs werden in der Datei "Dlgs. h" definiert.
2.  Verwenden Sie die [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur, um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das Flag " **\_ enableprinttemplate** " im **Flags** -Member fest. Verwenden Sie die **HINSTANCE** -und **lpprinttemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren.

        -Oder-

    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das Flag " **\_ enableprinttemplatehandle** " für PD fest. Verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

3.  Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie ein Rückruf Objekt bereitstellen, um Eingaben für die Steuerelemente zu verarbeiten. Das Rückruf Objekt implementiert eine [**iprintdialogcallback:: Lenker Message**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) -Methode, die an das benutzerdefinierte Dialogfeld gesendete Nachrichten empfängt.

So stellen Sie zusätzliche Eigenschaften Seiten bereit

1.  Verwenden Sie die-Funktion, um die zusätzlichen Seiten zu erstellen.
2.  Verwenden Sie den **lphpropertypages** -Member der [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur, um ein Array von Handles für die zusätzlichen Seiten anzugeben.

    Die Dialogfeld Prozeduren, die angegeben wurden, als Sie die Seiten Nachrichten für den Seiten Prozess erstellt haben.

3.  Möglicherweise möchten Sie ein Rückruf Objekt bereitstellen, das die-Schnittstelle implementiert. Die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion verwendet diese Schnittstelle, um einen Zeiger auf eine [**iprintdialogservices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) -Schnittstelle an die Anwendung zu übergeben. Die Dialogfeld Prozeduren für die zusätzlichen Eigenschaften Seiten können diese Schnittstelle verwenden, um Informationen über den aktuell ausgewählten Drucker abzurufen.

## <a name="callback-object-for-the-print-property-sheet"></a>Rückruf Objekt für das Druckeigenschaften Blatt

Eine Anwendung, die ein **Druck** Eigenschaften Blatt anzeigt, kann ein Rückruf Objekt implementieren, um Benachrichtigungen und Meldungen von der [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion zu empfangen, während das Eigenschaften Blatt angezeigt wird. Zum Bereitstellen eines Rückruf Objekts geben Sie einen Zeiger auf das Objekt im **lpcallback** -Member der [**printdlgex**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) -Struktur an.

Das Rückruf Objekt muss die [**iprintdialogcallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) -Schnittstelle implementieren. Die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion ruft in den folgenden Situationen **iprintdialogcallback** -Methoden auf:

-   Wenn das Dialogfeld initialisiert wurde
-   Wenn der Benutzer einen anderen Drucker aus der Liste der installierten Drucker auswählt, die auf dem Eigenschaften Blatt angezeigt werden.
-   Beim Empfang von Nachrichten für das untergeordnete Dialogfeld im unteren Teil der Seite **Allgemein** der Eigenschaften Seite

Das Rückruf Objekt sollte auch die [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) -Schnittstelle implementieren. Die [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion Ruft die-Methode auf, um einen Zeiger auf eine [**iprintdialogservices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) -Schnittstelle an eine Anwendung zu übergeben. Die [**iprintdialogcallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) -Methoden können die **iprintdialogservices** -Schnittstelle verwenden, um Informationen über den aktuell ausgewählten Drucker abzurufen. Die **iprintdialogservices** -Schnittstelle ist auch nützlich für Anwendungen, die zusätzliche Seiten erstellen, die auf der Seite **Allgemein** der **Druck** Eigenschaften Seite befolgt werden. Die Dialogfeld Prozeduren für die zusätzlichen Seiten können **iprintdialogservices** -Methoden aufrufen.

 

 