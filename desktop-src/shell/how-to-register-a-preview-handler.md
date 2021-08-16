---
description: In diesem Thema wird erläutert, wie Sie einen Einem bestimmten Datentyp zugeordneten Vorschauhandler registrieren.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Registrieren eines Vorschauhandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e1879261750609015acee2ccea1bc6f48f82df78ac7c18cbb2f46fa493c4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223439"
---
# <a name="how-to-register-a-preview-handler"></a>Registrieren eines Vorschauhandlers

In diesem Thema wird erläutert, wie Sie einen Einem bestimmten Datentyp zugeordneten Vorschauhandler registrieren. Zur Veranschaulichung wird in den Beispielen in diesem Thema der Dateityp .xyz verwendet. Die Registrierung eines Vorschauhandlers ist eine standarddateiassozbasierte Registrierung.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Zunächst wird eine Dateierweiterung einer ProgID zugeordnet. Der folgende Eintrag ordnet den **Unterschlüssel xyzfile** ProgID der Dateierweiterung .xyz zu.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

Der **Unterschlüssel xyzfile** ProgID wird wie hier gezeigt mit den anderen ProgIDs gespeichert:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Jeder Unterschlüssel des Vorschauhandlers ProgID enthält einen Unterschlüssel namens **shellex,** der immer den Unterschlüssel  **{8895b1c6-b41f-4c1c-a562-0d564250836f} enthält.** Das Vorhandensein dieses Unterschlüssels teilt dem System mit, dass der Handler ein Vorschauhandler ist.

Der Standardwert des Unterschlüssels **{8895b1c6-b41f-4c1c-a562-0d564250836f}** ist der Klassenbezeichner (CLSID) Ihres Handlers. Hier wird ein Beispiel für den **Xyzfile** ProgID-Unterschlüssel gezeigt, in dem ein Handler der CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154} zugeordnet wird.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Schritt 2:

Fügen Sie als Nächstes den Unterschlüssel unter **CLSID** für Ihren Vorschauhandler hinzu. Ein Beispiel finden Sie hier. Es folgt eine Erläuterung einzelner Einträge.

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

Der Standardwert für Ihren Unterschlüssel (hier **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) ist nicht erforderlich oder wird nicht verwendet. Wenn Sie sie jedoch auf eine nicht lokalisierte Zeichenfolge festlegen, können Sie Probleme bei der Registrierung debuggen.

Das Minuszeichen (-101) in der .dll im Eintrag DisplayName ist aus Legacygründen vorhanden. Der Symboleintrag erfordert dagegen kein Minuszeichen.

Der AppID-Wert gibt einen Verweis auf die AppID der Anwendung an, die der Dateierweiterung zugeordnet ist (gespeichert unter **HKEY \_ CLASSES \_ ROOT** \\ **APPID**). Der hier verwendete Wert ({6d2b5079-2f0b-48dd-ab7f-97cec514d30b}) ist die ID des Prevhost.exe-Ersatzzeichenhosts. 32-Bit-Vorschauhandler sollten **appID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} verwenden, wenn sie auf 64-Bit-Betriebssystemen installiert sind.

Die Einträge unter dem **Unterschlüssel InprocServer32** enthalten einen Verweis zurück auf den ProgID-Unterschlüssel der Dateierweiterung sowie einen Eintrag für [eine VersionIndependentProgID](../com/versionindependentprogid.md).

### <a name="step-3"></a>Schritt 3:

Schließlich muss der Vorschauhandler der Liste aller Vorschauhandler hinzugefügt werden. Diese Liste wird als Optimierung durch das System verwendet, um alle registrierten Vorschauhandler zu Anzeigezwecken aufzählen. Auch hier ist der Standardwert nicht erforderlich, er unterstützt lediglich den Debugvorgang.

> [!Note]  
> In Windows 7 verwenden Sie HKEY LOCAL MACHINE, wenn die Anwendung für alle Benutzer des Computers installiert ist. Verwenden Sie HKEY CURRENT USER, wenn nur ein Benutzer \_ \_ verwendet \_ \_ wird.

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorschauhandler und Shell-Vorschauhost](preview-handlers.md)
</dt> <dt>

[Erstellen von Vorschauhandlern](building-preview-handlers.md)
</dt> <dt>

[Richtlinien für Vorschauhandler](preview-handler-guidelines.md)
</dt> </dl>

 

 
