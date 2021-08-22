---
description: Die MsiEmbeddedUI-Tabelle definiert eine Benutzeroberfläche, die in das paket Windows Installer eingebettet ist.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: MsiEmbeddedUI-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7357a0b5aa1de2218eefb58fa85fbe374e9796ad0aaa94946743f1c51d9c8daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012948"
---
# <a name="msiembeddedui-table"></a>MsiEmbeddedUI-Tabelle

Die MsiEmbeddedUI-Tabelle definiert eine Benutzeroberfläche, die in das paket Windows Installer eingebettet ist.

**[Windows Installer 4.0 oder früher:](not-supported-in-windows-installer-4-0.md)** Wird nicht unterstützt. Diese Tabelle ist ab Windows Installer 4.5 verfügbar.

Die MsiEmbeddedUI-Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ                               | Key | Nullwerte zulässig |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [Identifier](identifier.md)       | J   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| Attribute    | [Integer](integer.md)             | N   | N        |
| Messagefilter | [DoubleInteger](doubleinteger.md) | N   | J        |
| Daten          | [Binär (Binary)](binary.md)               | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

Der Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Dateiname
</dt> <dd>

Der Name der Datei, die die Binärinformationen in der Spalte Daten empfängt. Der Name der Datei muss eine Erweiterung enthalten. Beispielsweise ist der Name *embeddedui.dll* akzeptabel, *aber embeddedui* ist nicht akzeptabel. Der Name kann lokalisiert werden. Dieses Feld kann einen kurzen Dateinamen oder einen langen Dateinamen enthalten, aber nicht beides. Das Format dieses Felds entspricht dem Datentyp der [Spalte Dateiname,](filename.md) mit der Ausnahme, dass das \| vertikale Balkentrennzeichen () für die Syntax für kurze Dateinamen/lange Dateinamen nicht verfügbar ist. Da bei einigen Webservern die Groß-/Kleinschreibung beachtet werden kann, sollte FileName genau mit der Groß-/Kleinschreibung der Quelldateien übereinstimmen, um die Unterstützung von Internetdownloads sicherzustellen.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Informationen zu den Daten in der Spalte Daten. Der Wert in diesem Feld kann eine oder mehrere der folgenden Konstanten enthalten.



| Konstante                      | Hexadezimal | Decimal | Bedeutung                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine                          | 0x00        | 0       | Die Datei ist nicht die DLL-Datei für die Benutzeroberfläche. Dabei kann es sich um eine ressourcendatei, die von der Benutzeroberfläche verwendet wird.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | Die primäre DLL-Datei für die Benutzeroberfläche. Nicht mehr als eine Zeile in der Tabelle kann mit diesem Attribut markiert werden. Wenn mehrere Zeilen mit diesem Attribut markiert sind, ist dies ein Fehler, und es kann nicht garantiert werden, welche DLL verwendet wird. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Ermöglicht dem Installationsprogramm, die eingebettete Benutzeroberfläche während einer Einfachinstallation auf Benutzeroberflächenebene aufzurufen. Das Installationsprogramm ignoriert dieses Attribut, wenn es nicht mit dem **msidbEmbeddedUI-Attribut** kombiniert wird.                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>Messagefilter
</dt> <dd>

Gibt die Typen von Nachrichten an, die an die Benutzeroberflächen-DLL gesendet werden. Diese Spalte ist nur für Zeilen mit dem **msidbEmbeddedUI-Attribut** relevant. Dieses Feld sollte NULL sein, wenn eine Zeile auf eine Ressourcendatei verweist und der Wert von Attribute NULL ist. Wenn eine Zeile auf eine Benutzeroberflächen-DLL verweist, darf der Wert in dieser Spalte nicht NULL sein.

Der Wert in dieser Spalte kann eine Kombination der folgenden Werte sein. Das Installationsprogramm ignoriert alle anderen Werte.



| Konstante                           | Hexadezimal | Decimal   | Beschreibung                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | Vorzeitige Beendigung.                                                                                       |
| **\_INSTALLLOGMODE-FEHLER**          | 0x00002     | 2         | Fehlermeldungen                                                                                              |
| **\_INSTALLLOGMODE-WARNUNG**        | 0x00004     | 4         | Warnmeldungen.                                                                                            |
| **INSTALLLOGMODE \_ USER**           | 0x00008     | 8         | Benutzernachrichten.                                                                                               |
| **INSTALLLOGMODE \_ INFO**           | 0x00010     | 16        | Nicht protokollierte Statusmeldungen.                                                                                    |
| **INSTALLLOGMODE \_ FILESINUSE**     | 0x00020     | 32        | Dateien, die derzeit verwendet werden.                                                                                 |
| **INSTALLLOGMODE \_ RESOLVESOURCE**  | 0x00040     | 64        | Quellauflösungsanforderungen.                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | Datenträgerspeicherplatzmeldungen.                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | Aktionsstartmeldungen.                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | Aktionsdatenmeldungen.                                                                                        |
| **INSTALLLOGMODE \_ PROGRESS**       | 0x00400     | 1024      | Statusmeldungen.                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2048      | Meldungen zur Benutzeroberflächeninitialisierung.                                                                                  |
| **INSTALLLOGMODE \_ INITIALIZE**     | 0x01000     | 4096      | Benutzeroberflächenstartmeldungen, die gesendet werden, wenn eine Produktinstallation gestartet wird.                                            |
| **INSTALLLOGMODE \_ TERMINATE**      | 0x02000     | 8192      | Meldungen zum Herunterfahren der Benutzeroberfläche, die nach Abschluss einer Produktinstallation gesendet werden.                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | Nachrichten, die vor der Anzeige des Dialogfelds "Benutzeroberfläche" gesendet werden.                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | Dateien, die derzeit verwendet werden.                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | Die Installation des Produkts beginnt. Die Nachricht enthält productName und ProductCode des Produkts.              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | Die Installation des Produkts endet. Die Nachricht enthält productName, ProductCode und den Rückgabewert des Produkts. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Diese Spalte enthält binäre Informationen. Wenn das Attributfeld mit dem **msidbEmbeddedUI-Attribut** markiert ist, müssen die Informationen in diesem Feld eine DLL sein. Wenn das Attributfeld nicht das **msidbEmbeddedUI-Attribut** ist, können die Informationen in diesem Feld eine Ressourcendatei in einem beliebigen Format sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um eine eingebettete Benutzeroberfläche verwenden zu können, muss der Setupentwickler diese Funktionalität im Windows Installer-Paket erstellen. Die Tabelle MsiEmbeddedUI definiert die eingebettete Benutzeroberfläche. Die DLL für die eingebettete Benutzeroberfläche sollte die Funktionen *InitializeEmbeddedUI,* *EmbeddedUIHandler* und *ShutdownEmbeddedUI* exportieren. Pakete, die keine eingebettete Benutzeroberfläche unterstützen, können die interne Benutzeroberfläche Windows Installer verwenden.

Um [Debugtools für Windows](https://www.microsoft.com/?ref=go) auf einer eingebetteten Benutzeroberfläche auszuführen, verwenden Sie die unter [Debuggen von benutzerdefinierten Aktionen](debugging-custom-actions.md)beschriebenen Verfahren. Legen Sie den Wert von MsiBreak auf MsiEmbeddedUI fest.

Ein Beispiel für eine eingebettete benutzerdefinierte Benutzeroberfläche finden Sie unter [Verwenden einer eingebetteten Benutzeroberfläche.](using-an-embedded-ui.md)

 

 



