---
description: In diesem Thema wird erläutert, wie sie einen Vorschauhandler registrieren, der einem bestimmten Datentyp zugeordnet ist.
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

In diesem Thema wird erläutert, wie sie einen Vorschauhandler registrieren, der einem bestimmten Datentyp zugeordnet ist. Zur Veranschaulichung verwenden die Beispiele in diesem Thema den Dateityp .xyz. Die Registrierung eines Vorschauhandlers ist eine standarddateizuordnungsbasierte Registrierung.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Zunächst wird eine Dateinamenerweiterung einer ProgID zugeordnet. Der folgende Eintrag ordnet den **Xyzfile-Unterschlüssel** ProgID der Dateinamenerweiterung .xyz zu.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

Der **Xyzfile-Unterschlüssel** ProgID wird wie hier gezeigt zusammen mit den anderen ProgIDs gespeichert:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Jeder ProgID-Unterschlüssel des Vorschauhandlers enthält einen Unterschlüssel namens **shellex,** der einen Unterschlüssel mit *dem Namen* **{8895b1c6-b41f-4c1c-a562-0d564250836f}** enthält. Das Vorhandensein dieses Unterschlüssels weist das System an, dass der Handler ein Vorschauhandler ist.

Der Standardwert des **Unterschlüssels {8895b1c6-b41f-4c1c-a562-0d564250836f}** ist der Klassenbezeichner (CLSID) Ihres Handlers. Ein Beispiel für den **Xyzfile-Unterschlüssel** ProgID wird hier gezeigt, in dem ein Handler der CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154} zugeordnet wird.

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

Der Standardwert für Ihren Unterschlüssel (hier **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) ist nicht erforderlich oder wird nicht verwendet. Wenn Sie sie jedoch auf eine nicht lokalisierte Zeichenfolge festlegen, können Sie Registrierungsprobleme debuggen.

Das Minuszeichen (-101) in der .dll Ressource im Eintrag DisplayName ist aus Legacygründen vorhanden. Für den Eintrag Symbol ist dagegen kein Minuszeichen erforderlich.

Der AppID-Wert gibt einen Verweis auf die AppID der Anwendung an, die der Dateinamenerweiterung zugeordnet ist (gespeichert unter **HKEY \_ CLASSES \_ ROOT** \\ **APPID**. Der hier verwendete Wert {6d2b5079-2f0b-48dd-ab7f-97cec514d30b} ist die ID des Prevhost.exe Ersatzhosts. 32-Bit-Vorschauhandler sollten **appID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} verwenden, wenn sie unter 64-Bit-Betriebssystemen installiert sind.

Die Einträge unter dem **Unterschlüssel InprocServer32** enthalten einen Verweis zurück auf den ProgID-Unterschlüssel der Dateinamenerweiterung sowie einen Eintrag für [versionIndependentProgID.](../com/versionindependentprogid.md)

### <a name="step-3"></a>Schritt 3:

Schließlich muss der Vorschauhandler der Liste aller Vorschauhandler hinzugefügt werden. Diese Liste wird vom System als Optimierung verwendet, um alle registrierten Vorschauhandler zu Anzeigezwecken aufzulisten. Auch hier ist der Standardwert nicht erforderlich, sondern unterstützt lediglich den Debugprozess.

> [!Note]  
> Wenn die Anwendung in Windows 7 für alle Benutzer des Computers installiert ist, verwenden Sie HKEY \_ LOCAL \_ MACHINE. Wenn nur für einen Benutzer HKEY CURRENT USER verwendet \_ \_ wird.

 

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

 

 
