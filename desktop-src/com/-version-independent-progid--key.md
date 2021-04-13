---
title: Versions unabhängiger ProgID-Schlüssel
description: Ordnet eine ProgID einer CLSID zu. Dieser Schlüssel wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474910"
---
# <a name="version-independent-progid-key"></a>Versions unabhängiger ProgID-Schlüssel

Ordnet eine ProgID einer CLSID zu. Dieser Schlüssel wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Bemerkungen

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

Das Format für <*Versions unabhängige ProgID*> ist <*Programm*>. <*Komponenten*>, getrennt durch Punkte, keine Leerzeichen und keine Versionsnummer. Die Versions unabhängige ProgID, wie z. b. die ProgID, kann mit einem lesbaren Namen registriert werden.

*ProgID* ist die ProgID der neuesten installierten Version der-Klasse.

Anwendungen müssen einen Versions unabhängigen programmatischen Bezeichner unter dem *Versions unabhängigen ProgID-* Schlüssel registrieren. Die Versions unabhängige ProgID bezieht sich auf die-Klasse der Anwendung und ändert sich nicht von Version zu Version, sondern bleibt für alle Versionen von Microsoft Word unverändert. Sie wird mit Makro Sprachen verwendet und verweist auf die aktuell installierte Version der-Klasse der Anwendung. Die Versions unabhängige ProgID muss mit dem Namen der aktuellen Version der Objekt Anwendung übereinstimmen.

Beispielsweise wird die Versions unabhängige ProgID verwendet, wenn eine Containeranwendung ein Diagramm oder eine Tabelle mit einer Symbolleisten Schaltfläche erstellt. In dieser Situation kann die Anwendung die Versions unabhängige ProgID verwenden, um die neueste Version der benötigten Objekt Anwendung zu ermitteln.

Die Versions unabhängige ProgID wird nur durch den Anwendungscode gespeichert und verwaltet. Wenn die Versions unabhängige ProgID angegeben ist, gibt die [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) -Funktion die CLSID der aktuellen Version zurück.

Sie können [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**progidfromclsid**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) verwenden, um zwischen diesen beiden Darstellungen zu konvertieren.

Sie können [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) oder [**olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) verwenden, um den Bezeichner in eine anzeigbare Zeichenfolge zu ändern.

Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf OLE32.DLL festgelegt werden, wie im folgenden Beispiel gezeigt:

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**Progidfromclsid**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<ProgID> Wichtigen](-progid--key.md)
</dt> </dl>

 

 




