---
title: Sicherheitsaspekte Microsoft Windows-Steuerelemente
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows-Steuerelementen.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102499"
---
# <a name="security-considerations-microsoft-windows-controls"></a>Überlegungen zur Sicherheit: Microsoft Windows-Steuerelemente

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows-Steuerelementen. Die Informationen in diesem Thema enthalten nicht alles, was Sie über Sicherheitsprobleme wissen müssen – Sie können es als Ausgangspunkt und Referenz für diesen Technologiebereich verwenden.

Die Konnektivität zwischen Computern ist üblich. der Hauptanliegen eines Entwicklers ist die Anwendungssicherheit. In den folgenden Abschnitten werden einige mögliche Sicherheitsprobleme erläutert, die beim Programmieren von Windows-Steuerelementen berücksichtigt werden

-   [Mit NULL beendete Steuerungs Meldungen](#null-terminated-control-messages)
-   [Zeichen folgen Verwendung](#string-use)
-   [Eingabevalidierung](#input-validation)
-   [Kenn Wort Verwendung](#password-use)
-   [Sicherheitswarnungen](#security-alerts)
-   [Zugehörige Themen](#related-topics)

## <a name="null-terminated-control-messages"></a>Mit NULL beendete Steuerungs Meldungen

Viele der Steuerungs Meldungen und Makros verfügen über Zeichen folgen Parameter. Diese Nachrichten überprüfen häufig nicht die Eingabe Zeichenfolgen, insbesondere nicht, um eine abschließende zu überprüfen `'\0'` . Wenn Sie eine Nachricht aufrufen, die eine Zeichenfolge als Parameter verwendet, geben Sie explizit an, dass die Zeichenfolge NULL-terminiert ist.

## <a name="string-use"></a>Zeichen folgen Verwendung

Beim Programmieren von Windows-Steuerelementen ist es erforderlich, Zeichen folgen zu bearbeiten. Fast jedes Steuerelement erfordert, dass Text eingefügt wird. Um z. b. ein Listenfeld aufzufüllen, müssen Sie Zeichen folgen in das-Steuerelement laden. Da die Verwendung von Zeichen folgen fälschlicherweise zu Pufferüberläufen führt, sollten Sie Vorkehrungen treffen, um dieses Sicherheitsrisiko zu vermeiden.

Weitere Informationen zu Pufferüberläufen finden Sie unter *Schreiben von sicherem Code* von Michael Howard und David LeBlanc, Microsoft Press, 2002 und [bewährten Methoden für die Sicherheits-APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>Eingabeüberprüfung

Die folgenden Steuerungs Meldungen können Sicherheitsprobleme darstellen.

-   [**CB \_ getlbtext**](cb-getlbtext.md)
-   [**LVM \_ getisearchstring**](lvm-getisearchstring.md)
-   [**SB \_ gettext**](sb-gettext.md)
-   [**SB \_ GetTipText**](sb-gettiptext.md)
-   [**TB \_ getbuttontext**](tb-getbuttontext.md)
-   [**TTM \_ gettext**](ttm-gettext.md)
-   [**TVM \_ getisearchstring**](tvm-getisearchstring.md)

Wenn der Text zwischen dem Aufruf zum Abrufen der Textlänge und dem Zeitpunkt, zu dem der Text angezeigt oder verwendet wird, geändert wird, kann ein Pufferüberlauf auftreten. Um dies zu vermeiden, müssen Sie die Zeichenfolge validieren, bevor Sie Sie verwenden. Außerdem verfügen die Nachrichten, die Text, [**CB \_ getlbtext**](cb-getlbtext.md), [**TB \_ getbuttontext**](tb-getbuttontext.md)und [**TTM \_ gettext**](ttm-gettext.md)abrufen, nicht über einen Parameter für die Puffergröße, der das Potenzial für einen Pufferüberlauf darstellt.

Wenn Sie [**CB \_ getlbtext**](cb-getlbtext.md) oder [**SB \_ gettext**](sb-gettext.md)verwenden, sollten Sie zuerst [**CB \_ getlbtextlen**](cb-getlbtextlen.md) oder [**SB \_ getTextLength**](sb-gettextlength.md) aufrufen, um die Puffergröße zu erhalten. Einige dieser Nachrichten, [**TB \_ getbuttontext**](tb-getbuttontext.md), [**LVM \_ getisearchstring**](lvm-getisearchstring.md)und [**TVM \_ getisearchstring**](tvm-getisearchstring.md)können mit einem **null** -Parameterwert aufgerufen werden, um die Länge der Zeichenfolge zu erhalten, bevor die Nachricht zum Abrufen der Zeichenfolge aufgerufen wird.

Eine Meldung, auf die Sie besonders achten sollten, ist die Statusleiste [**SB \_ GetTipText**](sb-gettiptext.md) Message. Diese Meldung bietet keine Möglichkeit, die Länge der abzurufenden Zeichenfolge abzufragen.

## <a name="password-use"></a>Kenn Wort Verwendung

Wenn Sie Kenn Wort geschütztes Bearbeitungs Steuerelemente ([**es \_**](edit-control-styles.md) -Kenn Wort Format) verwenden, muss der Puffer, der den abgerufenen Text enthält, so bald wie möglich auf NULL festgelegt werden, um zu vermeiden, dass das Kennwort des Benutzers im Speicher verfügbar gemacht

## <a name="security-alerts"></a>Sicherheitswarnungen

In der folgenden Tabelle sind die Funktionen aufgelistet, die bei falscher Verwendung die Sicherheit Ihrer Anwendungen beeinträchtigen können. Die hier aufgeführten Meldungen stellen keinen Parameter bereit, der die Puffergröße angibt.



| Funktion                                               | Minderung                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dlgdirlistcombobox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Stellen Sie sicher, dass der von der Funktion verwendete Puffer in geschrieben werden kann und auf NULL endet.                                                                     |
| [**CB \_ getlbtext**](cb-getlbtext.md)                 | Rufen Sie [**CB \_ getlbtextlen**](cb-getlbtextlen.md) auf, um die Puffergröße zu erhalten, und rufen Sie dann [**CB \_ getlbtext**](cb-getlbtext.md) auf, um die Zeichenfolge abzurufen. |
| [**LVM \_ getisearchstring**](lvm-getisearchstring.md) | Rufen Sie die Nachricht mit einem **null** -Parameterwert auf, um die Puffergröße zu erhalten, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.             |
| [**SB \_ gettext**](sb-gettext.md)                     | Rufen Sie [**SB \_ getTextLength**](sb-gettextlength.md) auf, um die Puffergröße zu erhalten, und rufen Sie dann [**SB \_ gettext**](sb-gettext.md) auf, um die Zeichenfolge abzurufen.   |
| [**TB \_ getbuttontext**](tb-getbuttontext.md)         | Rufen Sie die Nachricht mit einem **null** -Parameterwert auf, um die Puffergröße zu erhalten, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.             |
| [**TTM \_ gettext**](ttm-gettext.md)                   | Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu erkennen oder anzugeben.                                                                  |
| [**TVM \_ getisearchstring**](tvm-getisearchstring.md) | Rufen Sie die Meldung auf, indem Sie einen **null** -Parameterwert übergeben, um die Puffergröße zu erhalten, und dann die Nachricht ein zweites Mal aufrufen, um die Zeichenfolge abzurufen.       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Security](/windows/desktop/security)
</dt> <dt>

[TechNet-Sicherheitsressourcen](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Bewährte Methoden für die Sicherheits-APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 