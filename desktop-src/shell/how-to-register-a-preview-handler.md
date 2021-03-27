---
description: In diesem Thema wird erläutert, wie ein Vorschau Handler registriert wird, der einem bestimmten Datentyp zugeordnet ist.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Registrieren eines Vorschau Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979520"
---
# <a name="how-to-register-a-preview-handler"></a>Registrieren eines Vorschau Handlers

In diesem Thema wird erläutert, wie ein Vorschau Handler registriert wird, der einem bestimmten Datentyp zugeordnet ist. Zum Zweck der Veranschaulichung wird in den Beispielen in diesem Thema der Dateityp ". xyz" verwendet. Die Registrierung eines Vorschau Handlers ist eine standardmäßige Datei Zuordnungs basierte Registrierung.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Zuerst wird eine Dateinamenerweiterung einer ProgID zugeordnet. Der folgende Eintrag ordnet den **xyzfile** ProgID-Unterschlüssel der Dateinamenerweiterung ". xyz" zu.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

Der Unterschlüssel **xyzfile** ProgID wird mit den anderen ProgIDs gespeichert, wie hier gezeigt:

```
HKEY_CLASSES_ROOT
   xyzfile
```

Jeder Vorschau Handler ProgID unter Key enthält einen Unterschlüssel namens **shellex** , der einen Unterschlüssel mit *dem Namen* **{8895b1c6-b41f -4c1c-A562-0d564250836f}** enthält. Wenn dieser Unterschlüssel vorhanden ist, wird dem System mitgeteilt, dass es sich bei dem Handler um einen Vorschau Handler handelt.

Der Standardwert des unter Schlüssels **{8895b1c6-b41s-4c1c-A562-0d564250836f}** ist der Klassen Bezeichner (CLSID) des Handlers. Ein Beispiel für den Unterschlüssel **xyzfile** ProgID finden Sie unterzuordnen eines Handlers von CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>Schritt 2:

Fügen Sie als nächstes den Unterschlüssel unter **CLSID** für Ihren Vorschau Handler hinzu. Hier sehen Sie ein Beispiel. Eine Erläuterung der einzelnen Einträge folgt.

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

Der Standardwert für den Unterschlüssel (hier **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) ist nicht erforderlich oder wird nicht verwendet. Die Festlegung auf eine nicht lokalisierte Zeichenfolge kann Ihnen jedoch helfen, Registrierungsprobleme zu debuggen.

Das Minuszeichen (-101) in der dll-Ressource im Display Name-Eintrag ist aus Legacy Gründen vorhanden. Der Symbol Eintrag hingegen erfordert kein Minuszeichen.

Der AppID-Wert gibt einen Verweis auf die AppID der Anwendung an, die der Dateinamenerweiterung (gespeichert unter **HKEY \_ Classes \_ root** \\ **AppID**) zugeordnet ist. Der hier verwendete Wert – {6d2b5079-2S b-48dd-ab7f -97cec514d30b} – ist die ID des Prevhost.exe Ersatz Zeichen Hosts. 32-Bit-Vorschau Handler sollten bei der Installation auf 64-Bit-Betriebssystemen **AppID** {534a1e02-d58fi-44fi0-b58b-36cbed287c7c} verwenden.

Die Einträge unter dem **InProcServer32** -Unterschlüssel enthalten einen Verweis auf den ProgID-Unterschlüssel der Dateinamenerweiterung sowie einen Eintrag für eine [VersionIndependentProgId](../com/versionindependentprogid.md).

### <a name="step-3"></a>Schritt 3:

Schließlich muss der Vorschau Handler der Liste aller Vorschau Handler hinzugefügt werden. Diese Liste wird vom System als Optimierung verwendet, um alle registrierten Vorschau Handler zu Anzeige Zwecken aufzuzählen. Der Standardwert ist zwar nicht erforderlich, er hilft einfach beim Debugprozess.

> [!Note]  
> Wenn die Anwendung für alle Benutzer des Computers installiert ist, verwenden Sie unter Windows 7 HKEY \_ local \_ Machine. Wenn Sie nur für einen Benutzer den aktuellen HKEY- \_ Benutzer verwenden \_ .

 

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

[Vorschau Handler und Shell-Vorschau Host](preview-handlers.md)
</dt> <dt>

[Entwickeln von Vorschau Handlern](building-preview-handlers.md)
</dt> <dt>

[Vorschau der handlerrichtlinien](preview-handler-guidelines.md)
</dt> </dl>

 

 
