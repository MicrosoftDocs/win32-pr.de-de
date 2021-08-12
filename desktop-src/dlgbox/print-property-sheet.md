---
title: Eigenschaftenblatt drucken
description: Das Eigenschaftenblatt Drucken ist eine Standard-Benutzeroberfläche, mit der der Benutzer die Eigenschaften eines bestimmten Druckauftrags angeben kann.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Windows Benutzeroberfläche,Benutzereingabe
- Windows Benutzeroberfläche,Common Dialog Box Library
- Benutzereingabe,Allgemeine Dialogfeldbibliothek
- Erfassen von Benutzereingaben,Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Eigenschaftenblatt drucken (Dialogfeld)
- Anpassen des Dialogfelds "Druckeigenschaftenblatt"
- Vordefinierte Dialogfelder
- Dialogfelder,Eigenschaftenblatt drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54bc8065ada207702755e8fc0a1586620f660db9f3acf2a67e32b56e393143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280508"
---
# <a name="print-property-sheet"></a>Eigenschaftenblatt drucken

Das **Eigenschaftenblatt** Drucken ist eine Standard-Benutzeroberfläche, mit der der Benutzer die Eigenschaften eines bestimmten Druckauftrags angeben kann. Das Eigenschaftenblatt besteht aus einer Reihe von Eigenschaftenseiten, die je nach Drucker oder Anwendung variieren. Zu einer Teilmenge Windows Standard-Eigenschaftenseiten können einige Drucker treiberspezifische Eigenschaftenseiten hinzufügen, und einige Anwendungen können anwendungsspezifische Eigenschaftenseiten hinzufügen.

Initialisieren Sie zum Erstellen und Anzeigen eines Druck-Eigenschaftenblatts eine [**PRINTDLGEX-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) und übergeben Sie die Struktur an die  [**PrintDlgEx-Funktion.**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))

Die folgende Abbildung zeigt ein typisches **Druckeigenschaftsblatt.**

![Druckereigenschaftsblatt](images/printerpropertypagexp.png)

Die meisten Member der [**PRINTDLGEX-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) sind identisch mit denen der [**PRINTDLG-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Beschreibungen zur Verwendung der allgemeinen Strukturelemente für die Interaktion mit den Dialogfeld-Steuerelementen finden Sie unter [Dialogfeld drucken.](print-dialog-box.md) Im weiteren Verlauf dieses Themas werden die **Eigenschaftenblattfeatures** drucken beschrieben, die sich vom **Dialogfeld Drucken** unterscheiden.

Sie können  ein Eigenschaftenblatt drucken anpassen, indem Sie eine benutzerdefinierte Dialogfeldvorlage für den unteren Teil der Seite Allgemein angeben und zusätzliche Eigenschaftenseiten angeben, die der Seite **Allgemein folgen.**  Weitere Informationen finden Sie unter [Anpassen des Druckeigenschaftsblatts.](#customizing-the-print-property-sheet)

Sie können ein Rückrufobjekt implementieren, um Benachrichtigungen und Nachrichten von der [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) zu empfangen, während das Eigenschaftenblatt angezeigt wird. Anwendungen, die benutzerdefinierte Vorlagen oder zusätzliche Seiten bereitstellen, verwenden das Rückrufobjekt für die Kommunikation mit dem Eigenschaftenblatt. Weitere Informationen finden Sie unter [Rückrufobjekt für das Druckeigenschaftsblatt](#callback-object-for-the-print-property-sheet).

Das **Eigenschaftenblatt** Drucken bietet Unterstützung für die Angabe mehrerer, nicht zusammenhängender Seitenbereiche, die gedruckt werden. Das **lpPageRanges-Element** der [**PRINTDLGEX-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) gibt ein Array von [**PRINTPAGERANGE-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) an, in denen jede Struktur einen Seitenbereich angibt.

Das **Eigenschaftenblatt** Drucken zeigt ein **Optionsfeld Aktuelle** Seite als Teil der Optionsfeldgruppe **Seitenbereich** an. Verwenden Sie zum **Steuern** des Optionsfelds Aktuelle Seite die **Flags PD \_ CURRENTPAGE** und **PD \_ NOCURRENTPAGE** im **Flags-Member** der [**PRINTDLGEX-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Anpassen des Druckeigenschaftsblatts](#customizing-the-print-property-sheet)
-   [Rückrufobjekt für das Druckeigenschaftsblatt](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Anpassen des Druckeigenschaftsblatts

Sie können das **Eigenschaftenblatt Drucken** wie folgt anpassen:

-   Geben Sie eine benutzerdefinierte Vorlage für den unteren Teil der Seite **Allgemein** an. Dadurch können Sie zusätzliche Steuerelemente verwenden, die für Ihre Anwendung eindeutig sind. Die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) verwendet ihre benutzerdefinierte Vorlage statt der Standardvorlage.
-   Stellen Sie zusätzliche Eigenschaftenseiten zur Verfügung, um der Seite **Allgemein zu** folgen.
-   Geben Sie ein Rückrufobjekt an. Weitere Informationen finden Sie unter [Rückrufobjekt für das Druckeigenschaftsblatt](#callback-object-for-the-print-property-sheet).

Sie können den oberen Teil der Seite Allgemein **nicht** ändern. Sie können die vom Druckertreiber bereitgestellten Eigenschaftenseiten nicht ändern.

So stellen Sie eine benutzerdefinierte Vorlage für die Seite Allgemein zur Verfügung:

1.  Erstellen Sie eine benutzerdefinierte Vorlage für den unteren Teil der Seite **Allgemein,** indem Sie die in der Datei Prnsetup.dlg angegebene PRINTDLGEXORD-Vorlage ändern. In der Regel muss die benutzerdefinierte Vorlage die gleiche Größe wie die Standardvorlage haben. Sie können die benutzerdefinierte Vorlage jedoch vergrößern, wenn Sie das **FLAG PD \_ USELARGETEMPLATE** angeben, um eine größere Seite **Allgemein zu** erstellen. Die steuerelementbezeichner, die in der Standardvorlage **des** Dialogfelds Drucken verwendet werden, werden in der Datei Dlgs.h definiert.
2.  Verwenden Sie [**die PRINTDLGEX-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder dynamic-link-Bibliothek ist, legen Sie das **PD \_ ENABLEPRINTTEMPLATE-Flag** im **Flags-Element** fest. Verwenden Sie **die Elemente hInstance** und **lpPrintTemplateName** der -Struktur, um das Modul und den Ressourcennamen zu identifizieren.

        -Oder-

    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **FLAG PD \_ ENABLEPRINTTEMPLATEHANDLE** fest. Verwenden Sie **den hInstance-Member,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

3.  Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie ein Rückrufobjekt bereitstellen, um Eingaben für Ihre Steuerelemente zu verarbeiten. Das Rückrufobjekt implementiert eine [**IPrintDialogCallback::HandleMessage-Methode,**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) die Nachrichten empfängt, die an das benutzerdefinierte Dialogfeld gesendet werden.

So stellen Sie zusätzliche Eigenschaftenseiten zur Verfügung

1.  Verwenden Sie die -Funktion, um die zusätzlichen Seiten zu erstellen.
2.  Verwenden Sie **das lphPropertyPages-Member** der [**PRINTDLGEX-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) um ein Array von Handles für die zusätzlichen Seiten anzugeben.

    Die dialogfeld-Prozeduren, die beim Erstellen der einzelnen Seiten angegeben wurden, verarbeiten nachrichten, die an die Seiten gesendet werden.

3.  Möglicherweise möchten Sie ein Rückrufobjekt bereitstellen, das die -Schnittstelle implementiert. Die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) verwendet diese Schnittstelle, um der Anwendung einen Zeiger auf eine [**IPrintDialogServices-Schnittstelle zu**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) übergeben. Die Dialogfeldverfahren für die zusätzlichen Eigenschaftenseiten können diese Schnittstelle verwenden, um Informationen zum aktuell ausgewählten Drucker abzurufen.

## <a name="callback-object-for-the-print-property-sheet"></a>Rückrufobjekt für das Druckeigenschaftsblatt

Eine Anwendung,  die ein Druck-Eigenschaftenblatt anzeigt, kann ein Rückrufobjekt implementieren, um Benachrichtigungen und Nachrichten von der [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) zu empfangen, während das Eigenschaftenblatt angezeigt wird. Um ein Rückrufobjekt anzugeben, geben Sie einen Zeiger auf das Objekt im **lpCallback-Member** der [**PRINTDLGEX-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) an.

Das Rückrufobjekt muss die [**IPrintDialogCallback-Schnittstelle**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) implementieren. Die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) ruft in den folgenden Situationen **IPrintDialogCallback-Methoden** auf:

-   Wenn das Dialogfeld initialisiert wurde
-   Wenn der Benutzer einen anderen Drucker aus der Liste der installierten Drucker auswählt, die auf dem Eigenschaftenblatt angezeigt werden
-   Beim Empfangen von Nachrichten für das untergeordnete Dialogfeld im unteren Teil der Seite Allgemein des **Eigenschaftenblatts**

Das Rückrufobjekt sollte auch die [**IObjectWithSite-Schnittstelle**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) implementieren. Die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) ruft die -Methode auf, um einen Zeiger auf eine [**IPrintDialogServices-Schnittstelle**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) an eine Anwendung zu übergeben. Die [**IPrintDialogCallback-Methoden**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) können die **IPrintDialogServices-Schnittstelle** verwenden, um Informationen zum aktuell ausgewählten Drucker abzurufen. Die **IPrintDialogServices-Schnittstelle** ist auch nützlich für Anwendungen, die zusätzliche Seiten erstellen, um der Seite **Allgemein** des **Eigenschaftenblatts Drucken** zu folgen. Die Dialogfeldverfahren für die zusätzlichen Seiten können **IPrintDialogServices-Methoden** aufrufen.

 

 