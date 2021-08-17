---
title: Sicherheitsüberlegungen zu Microsoft Windows Controls
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows Steuerelementen.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45faa0f3d2f521038c056055329d70541625bac88c16e62c1581b55ae2a6c5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696510"
---
# <a name="security-considerations-microsoft-windows-controls"></a>Sicherheitsüberlegungen: Microsoft Windows Controls

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows Steuerelementen. Die Informationen in diesem Thema bieten nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie sie als Ausgangspunkt und Referenz für diesen Technologiebereich.

Die Interkonnektivität zwischen Computern ist üblich. Das Hauptanliegen eines Entwicklers muss die Anwendungssicherheit sein. In den folgenden Abschnitten werden einige potenzielle Sicherheitsprobleme erläutert, die beim Programmieren von Windows werden sollten.

-   [Auf NULL beendete Steuerungsmeldungen](#null-terminated-control-messages)
-   [Zeichenfolgennutzung](#string-use)
-   [Eingabeüberprüfung](#input-validation)
-   [Kennwortnutzung](#password-use)
-   [Sicherheitswarnungen](#security-alerts)
-   [Zugehörige Themen](#related-topics)

## <a name="null-terminated-control-messages"></a>Auf NULL beendete Steuerungsmeldungen

Viele der Steuerungsmeldungen und Makros verfügen über Zeichenfolgenparameter. Häufig überprüfen diese Nachrichten die Eingabezeichenfolgen nicht, insbesondere nicht auf einen beendenden `'\0'` . Wenn Sie eine Nachricht aufrufen, die eine Zeichenfolge als Parameter verwendet, geben Sie explizit an, dass die Zeichenfolge null-terminiert ist.

## <a name="string-use"></a>Zeichenfolgennutzung

Wenn Sie Windows-Steuerelemente programmieren, müssen Zeichenfolgen bearbeitet werden. Fast jedes Steuerelement erfordert, dass Text eingefügt wird. Wenn Sie beispielsweise ein Listenfeld auffüllen möchten, müssen Sie Zeichenfolgen in das -Steuerelement laden. Da die falsche Verwendung von Zeichenfolgen häufig zu Pufferüberläufen führt, sollten Sie Vorsichtsmaßnahmen ergreifen, um dieses Sicherheitsrisiko zu vermeiden.

Weitere Informationen zu Pufferüberläufen finden Sie unter *Writing Secure Code* von Michael Soll und David LeBlanc, Microsoft Press, 2002 und Best Practices für die [Sicherheits-APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>Eingabeüberprüfung

Die folgenden Steuermeldungen können Sicherheitsprobleme verursachen.

-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)
-   [**SB \_ GETTEXT**](sb-gettext.md)
-   [**SB \_ GETTIPTEXT**](sb-gettiptext.md)
-   [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**TTM \_ GETTEXT**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

Wenn sich der Text zwischen dem Aufruf zum Erhalten der Textlänge und der Zeit ändert, in der der Text angezeigt oder verwendet wird, kann ein Pufferüberlauf auftreten. Um dies zu vermeiden, müssen Sie die Zeichenfolge überprüfen, bevor Sie sie verwenden. Darüber hinaus verfügen die Nachrichten, die Text abrufen, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)und [**TTM \_ GETTEXT**](ttm-gettext.md), über keinen Puffergrößenparameter, der das Potenzial für einen Pufferüberlauf bietet.

Wenn Sie [**CB \_ GETLBTEXT**](cb-getlbtext.md) oder [**SB \_ GETTEXT verwenden,**](sb-gettext.md)sollten Sie zuerst [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) oder [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) aufrufen, um die Puffergröße zu erhalten. Einige dieser Meldungen, [**TB \_ GETBUTTONTEXT,**](tb-getbuttontext.md) [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)und [**TVM \_ GETISEARCHSTRING,**](tvm-getisearchstring.md)können mit einem **NULL-Parameterwert** aufgerufen werden, um die Länge der Zeichenfolge abzurufen, bevor die Nachricht aufgerufen wird, um die Zeichenfolge abzurufen.

Eine Meldung, auf die Sie besonders achten sollten, ist die [**SB \_ GETTIPTEXT-Meldung**](sb-gettiptext.md) in der Statusleiste. Diese Meldung bietet keine Möglichkeit, die Länge der abzurufenden Zeichenfolge abfragt.

## <a name="password-use"></a>Kennwortnutzung

Wenn Sie kennwortgeschützte Bearbeitungssteuerelemente [**(ES \_ PASSWORD-Format)**](edit-control-styles.md) verwenden, muss der Puffer, der den abgerufenen Text enthält, so bald wie möglich auf 0 (null) festgelegt werden, um zu vermeiden, dass das Kennwort des Benutzers im Arbeitsspeicher verfügbar ist.

## <a name="security-alerts"></a>Sicherheitswarnungen

In der folgenden Tabelle sind Funktionen aufgeführt, die bei falscher Verwendung die Sicherheit Ihrer Anwendungen gefährden können. Die hier aufgeführten Meldungen enthalten keinen Parameter, der die Puffergröße angibt.



| Komponente                                               | Minderung                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Stellen Sie sicher, dass der von der Funktion verwendete Puffer in geschrieben werden kann und null-terminiert ist.                                                                     |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                 | Rufen [**Sie CB \_ GETLBTEXTLEN auf,**](cb-getlbtextlen.md) um die Puffergröße abzurufen, und rufen Sie [**dann CB \_ GETLBTEXT**](cb-getlbtext.md) auf, um die Zeichenfolge abzurufen. |
| [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md) | Rufen Sie die  Nachricht mit einem NULL-Parameterwert auf, um die Puffergröße abzurufen, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.             |
| [**SB \_ GETTEXT**](sb-gettext.md)                     | Rufen [**Sie SB \_ GETTEXTLENGTH auf,**](sb-gettextlength.md) um die Puffergröße abzurufen, und rufen Sie [**dann SB \_ GETTEXT**](sb-gettext.md) auf, um die Zeichenfolge abzurufen.   |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Rufen Sie die  Nachricht mit einem NULL-Parameterwert auf, um die Puffergröße abzurufen, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.             |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                   | Diese Meldung bietet Ihnen keine Möglichkeit, die Größe des Puffers zu kennen oder anzugeben.                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | Rufen Sie die  Meldung auf, indem Sie einen NULL-Parameterwert übergeben, um die Puffergröße abzurufen, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Sicherheit](/windows/desktop/security)
</dt> <dt>

[TechNet-Sicherheitsressourcen](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Bewährte Methoden für die Sicherheits-APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 