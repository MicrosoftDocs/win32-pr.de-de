---
description: Für Benutzer weltweit ist die Texteingabe Teil einer modernen Computerumgebung für Bloggen, Kommentieren, Tweeting, Instant Messaging oder jede andere Art von Texteingabe. In Windows 8 ist die Rechtschreibprüfung integriert, um Steuerelemente zu bearbeiten.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Informationen zur Rechtschreibprüfungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c15594be003b67a6e0c9df62e234e8076cd4ea213bc08468f3bb72698f51f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754940"
---
# <a name="about-the-spell-checking-api"></a>Informationen zur Rechtschreibprüfungs-API

Für Benutzer weltweit ist die Texteingabe Teil einer modernen Computerumgebung für Bloggen, Kommentieren, Tweeting, Instant Messaging oder jede andere Art von Texteingabe. In Windows 8 ist die Rechtschreibprüfung integriert, um Steuerelemente zu bearbeiten.

Entwickler können die Rechtschreibprüfungs-API in ihren Apps verwenden, um verfügbare Rechtschreibprüfungsdienste zu nutzen. Entwickler können auch Rechtschreibprüfungstools erstellen, die zu Anbietern werden und in das Windows integriert sind.

Die Rechtschreibprüfungs-API ist für die Verwendung durch professionelle C/C++-Entwickler von Windows Component Object Model-Apps (COM) konzipiert. Die Rechtschreibprüfungs-API wird nicht für die Verwendung in einem Windows oder ASP.NET unterstützt.

## <a name="versioning"></a>Versionskontrolle

Die Rechtschreibprüfungs-API ist ab dem Windows 8 oder Windows Server 2012. Zukünftige Ergänzungen der API werden verarbeitet, indem neue Schnittstellen erstellt werden, die mit [**queryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die vorhandenen bestimmt werden können.

## <a name="interfaces"></a>Schnittstellen

Alle Schnittstellen müssen freigegeben werden, wenn sie nicht mehr verwendet werden. Alle zurückgegebenen **LPWSTR-Zeichenfolgen** (und **LPOLESTR-Elemente** von [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) müssen mit [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) freigegeben werden, wenn sie nicht mehr verwendet werden.

## <a name="error-handling"></a>Fehlerbehandlung

Fehler werden als **HRESULT s** zurückgegeben. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) und [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) werden in dieser API nicht unterstützt. Fehler sind mit Ausnahme falscher Argumente nicht besonders umsetzbar.

Standardmäßige RPC-Fehlercodes können von einem der API-Aufrufe zurückgegeben werden, da sie nicht mehr proc sind. Es gelten standardmäßige RPC-Timeouts.

## <a name="security"></a>Sicherheit

Die Rechtschreibprüfungs-API kann externen Code (Rechtschreibprüfungsanbieter) laden. Dieser Code wird out-of-proc und in einem eingeschränkten Sicherheitskontext ausgeführt.

## <a name="dictionary-files"></a>Wörterbuchdateien

Die benutzerspezifischen Wörterbücher für eine Sprache, die den Inhalt für die Wortlisten Hinzugefügt, Ausgeschlossen und AutoKorrektur enthalten, befinden sich unter %AppData% \\ Microsoft \\ Spelling \\ *<language tag>* . Die Dateinamen sind default.dic (Hinzugefügt), default.exc (Ausgeschlossen) und default.acl (AutoCorrect). Die Dateien sind UTF-16 LE-Klartext, der mit der entsprechenden Byte order Mark (BOM) beginnen muss. Jede Zeile enthält ein Wort (in der Liste Hinzugefügte und ausgeschlossene Wörter) oder ein autocorrect-Paar mit den Wörtern, die durch einen vertikalen Balken (" ") (in der AutoCorrect-Wortliste) getrennt \| sind. Andere im Verzeichnis enthaltene DIC-, EXC- und ACL-Dateien werden vom Rechtschreibprüfungsdienst erkannt und den Benutzerwortlisten hinzugefügt. Diese Dateien gelten als schreibgeschützt und werden von der Rechtschreibprüfungs-API nicht geändert.

## <a name="installing-a-spell-checking-provider"></a>Installieren eines Rechtschreibprüfungsanbieters

Bei der Installation eines Rechtschreibprüfungsanbieters müssen alle von ihm verwendeten Dateien an einem Speicherort gespeichert werden, der Lesezugriff von der SID[(](../secauthz/security-identifiers.md)Sicherheits-ID ) "ALLE ANWENDUNGSPAKETE" zulässt. Die Installation in einem Ordner unter "Programme" funktioniert gut. Außerdem muss der Anbieter einige Schlüssel in der Registrierung festlegen, damit sie in der Rechtschreibprüfungs-API angezeigt werden. Sie kann sich entweder in der Struktur HKEY CURRENT USER oder in der HKEY LOCAL MACHINE-Struktur bewegen, je nachdem, ob sie nur für den aktuellen Benutzer oder alle \_ \_ Benutzer installiert werden \_ \_ soll.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



Das [Beispiel des Rechtschreibprüfungsanbieters](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) enthält ein Beispiel für die Registrierung, die zum Installieren eines Anbieters erforderlich ist.

Wenn Sie neue Rechtschreibprüfungsoptionen für einen Rechtschreibprüfungsanbieter erstellen, finden Sie unter [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) eine Anleitung zur Benennung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Rechtschreibprüfungs-API](spell-checker-api-reference.md)
</dt> <dt>

[Beispiel für rechtschreibprüfungsclient](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Beispiel für Rechtschreibprüfungsanbieter](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
