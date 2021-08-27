---
description: Die Shell verwendet einen Registrierungsunterschlüssel für programmgesteuerte Bezeichner (ProgID), um einer Anwendung einen Dateityp zu zuordnen und das Verhalten der Zuordnung zu steuern.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Programmgesteuerte Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf982f865fa8b856bc29c00a9b2371b88b34615b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467287"
---
# <a name="programmatic-identifiers"></a>Programmgesteuerte Bezeichner

Die Shell verwendet einen Registrierungsunterschlüssel für programmgesteuerte Bezeichner (ProgID), um einer Anwendung einen Dateityp zu zuordnen und das Verhalten der Zuordnung zu steuern. Die progID-Einträge, die für Dateizuordnungen verwendet werden, befinden sich in der Registrierung unter **HKEY \_ CLASSES \_ ROOT.**

Dieses Thema ist wie folgt organisiert:

-   [Programmgesteuerte Bezeichnerelemente, die von Dateizuordnungen verwendet werden](#programmatic-identifier-elements-used-by-file-associations)
-   [Verwenden von programmgesteuerten Bezeichnern mit Versionsbezeichnern](#using-versioned-programmatic-identifiers)
-   [Zugehörige Themen](#related-topics)

Weitere Informationen finden Sie unter [Registrieren eines Dateityps für eine neue Anwendung.](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Programmgesteuerte Bezeichnerelemente, die von Dateizuordnungen verwendet werden

Das richtige Format eines ProgID-Schlüsselnamens ist \[ *Vendor oder Application* \] . \[ *Komponente* \] . \[ *Version,* getrennt durch Punkte und ohne Leerzeichen, wie \] in Word.Doc.6. Der *Teil Version* ist optional, wird jedoch dringend empfohlen. Weitere Informationen finden Sie unter [Verwenden von programmgesteuerten Bezeichnern mit Versionsinformationen.](#using-versioned-programmatic-identifiers)

Ein ProgID-Unterschlüssel sollte die folgenden Elemente enthalten. Beachten Sie, dass einige Zeichenfolgendaten in diesem Schlüssel eine bestimmte Formatierung erfordern.




| Element | BESCHREIBUNG | 
|---------|-------------|
| <strong>(Standard)</strong> | Legen Sie den Standardeintrag des Unterschlüssels ProgID auf einen Anzeigenamen für diese ProgID fest, der dem Benutzer angezeigt werden kann. Die Verwendung dieses Eintrags zum Verwenden des Angezeigtennamens wird auf Systemen, auf denen Windows 2000 oder höher ausgeführt wird, durch den Eintrag FriendlyTypeName als veraltet festgelegt. Sie sollten diesen Wert jedoch aus Gründen der Abwärtskompatibilität festlegen.<br /> | 
| <strong>AllowSilentDefaultTakeOver</strong> (eingeführt in Windows 8) | Legen Sie diesen optionalen Eintrag fest, um zu signalisieren, Windows diese ProgID beim Bestimmen eines Standardhandlers für einen öffentlichen Dateityp ignorieren soll. Unabhängig davon, ob dieser Wert festgelegt ist, wird die ProgID weiterhin im OpenWith-Kontextmenü und -dialogfeld angezeigt. Dies ist ein REG_NONE Wert. | 
| <strong>AppUserModelID</strong> (eingeführt in Windows 7) | Legen Sie diesen optionalen Eintrag auf die explizite Anwendungsbenutzermodell-ID (AppUserModelID) der Anwendung fest, wenn die <strong></strong> Anwendung <strong></strong> eine explizite AppUserModelID verwendet und entweder die automatisch generierten Aktuellen oder häufigen Sprunglisten des Systems verwendet oder eine benutzerdefinierte Sprungliste. Wenn eine Anwendung eine explizite AppUserModelID verwendet und diesen Wert nicht festgelegt, werden elemente nicht in den Sprunglisten dieser Anwendung angezeigt. Dies ist eine REG_SZ Zeichenfolge. Weitere Informationen finden Sie unter <a href="appids.md">Anwendungsbenutzermodell-IDs (AppUserModelIDs).</a><br /> | 
| <strong>EditFlags</strong> | Legen Sie diesen optionalen Eintrag mithilfe von Flags aus der <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS-Enumeration</strong></a> fest. Der EditFlags-Eintrag steuert einige Aspekte der Shellbehandlung der Dateitypen, die mit dieser ProgID verknüpft sind. Sie können auch den EditFlags-Eintrag verwenden, um zu begrenzen, wie viel der Benutzer bestimmte Aspekte dieser Dateitypen mithilfe des Eigenschaftenblatts einer Datei ändern kann. Die <strong>für EditFlags verwendeten FILETYPEATTRIBUTEFLAGS-Werte</strong> sind binäre Werte, die so entworfen wurden, dass Sie mehrere Attribute in einem bitweisem OR-Vorgang zu einem einzelnen Wert kombinieren können. Dies ist ein REG_DWORD oder REG_BINARY Wert.<br /> | 
| <strong>FriendlyTypeName</strong> | Legen Sie diesen Eintrag auf einen Anzeigenamen für die ProgID fest, der dem Benutzer angezeigt werden kann. Aus Konsistenz-Grund sollte diese Zeichenfolge die gleichen Daten wie der Standardeintrag für diesen ProgID-Schlüssel enthalten. Dieser Eintrag kann entweder eine REG_SZ- oder REG_EXPAND_SZ-Zeichenfolge sein, muss jedoch als indirekte Zeichenfolge formatiert sein (ein vollqualifizierter Dateiname und Ressourcenwert, dem das @-Symbol vorangegangen ist), z. B. <em>@%SystemRoot%\shell32.dll,-154</em>.<br /> | 
| <strong>InfoTip</strong> | Legen Sie diesen Eintrag auf eine kurze Hilfemeldung fest, die die Shell für diese ProgID anzeigt. Der InfoTip-Eintrag wird in einem Dialogfeld mit der Maus angezeigt. Dieser Wert kann entweder eine REG_SZ oder REG_EXPAND_SZ sein, muss aber wie FriendlyTypeName als indirekte Zeichenfolge formatiert werden.<br /> | 
| <strong>CurVer</strong> | Legen Sie den Eintrag (Standard) dieses Unterschlüssels auf die aktuelle Version dieser ProgID fest.<br /><blockquote>[!Note]<br />Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</blockquote><br /> | 
| <strong>DefaultIcon</strong>. | Legen Sie den Eintrag (Standard) dieses Unterschlüssels auf das Standardsymbol fest, das Sie für Dateitypen anzeigen möchten, die dieser ProgID zugeordnet sind. Dieser Wert kann entweder eine REG_SZ- oder REG_EXPAND_SZ-Zeichenfolge sein, muss jedoch als vollqualifizierter Dateiname mit seinem ressourcenbasierten Wert angegeben werden, z. B. <em>%SystemRoot%\shell32.dll,-154</em>.<br /> | 




 

Im folgenden Registrierungsschlüsselbeispiel wird ein ProgID-Schlüsselknoten für die Dateiassoz veranschaulicht:

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>Verwenden von programmgesteuerten Bezeichnern mit Versionsbezeichnern

Eine ProgID mit Versionsversion ist eine ProgID, deren Version im Namen angegeben ist. Hierzu fügen Sie dem Namen in der Regel einen Zeitraum und die Versionsnummer hinzu. Beispiel:

-   Word.Document.6
-   Word.Document.8

Hierbei handelt es sich um ProgIDs mit Versionsversion mit den Versionen 6 bzw. 8. Wenn Sie über eine gleichzeitig installierte Anwendung verfügen, die mehrere Versionen Ihrer Anwendung unterstützt, verwenden Sie CurVer und versionsunabhängige ProgIDs. Andernfalls sollten CurVer- und versionsunabhängige ProgIDs vermieden werden, da sie zu Ineffizienz führen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren eines Dateityps für eine neue Anwendung](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypverifizierer](file-type-verifier.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 




