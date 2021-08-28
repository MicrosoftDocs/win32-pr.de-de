---
title: Versionsunabhängiger ProgID-Schlüssel
description: Ordnet eine ProgID einer CLSID zu. Dieser Schlüssel wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad09f9d86c2f34d93757e940c5262cd294485ad5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883149"
---
# <a name="version-independent-progid-key"></a>Versionsunabhängiger ProgID-Schlüssel

Ordnet eine ProgID einer CLSID zu. Dieser Schlüssel wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Hinweise

Der Schlüssel **HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** entspricht dem **\_ HKEY CLASSES \_ ROOT-Schlüssel,** der aus Kompatibilitätsgründen mit früheren Versionen von COM beibehalten wurde.

Das Format für <*versionsunabhängige ProgID->* ist <*Programm*>.<*Komponente*>, getrennt durch Zeiträume, leerzeichen und keine Versionsnummer. Die versionsunabhängige ProgID kann wie die ProgID mit einem für Menschen lesbaren Namen registriert werden.

*ProgID* ist die ProgID der neuesten installierten Version der -Klasse.

Anwendungen müssen einen versionsunabhängigen programmgesteuerten Bezeichner unter dem *versionsunabhängigen ProgID-Schlüssel* registrieren. Die versionsunabhängige ProgID bezieht sich auf die -Klasse der Anwendung und ändert sich nicht von Version zu Version, sondern bleibt in allen Versionen konstant– z.B. Microsoft Word-Dokument. Sie wird mit Makrosprachen verwendet und bezieht sich auf die derzeit installierte Version der -Klasse der Anwendung. Die versionsunabhängige ProgID muss dem Namen der neuesten Version der Objektanwendung entsprechen.

Beispielsweise wird die versionsunabhängige ProgID verwendet, wenn eine Containeranwendung ein Diagramm oder eine Tabelle mit einer Symbolleistenschaltfläche erstellt. In diesem Fall kann die Anwendung die versionsunabhängige ProgID verwenden, um die neueste Version der erforderlichen Objektanwendung zu ermitteln.

Die versionsunabhängige ProgID wird ausschließlich durch Anwendungscode gespeichert und verwaltet. Wenn die versionsunabhängige ProgID angegeben wird, gibt die [**CLSIDFromProgID-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) die CLSID der aktuellen Version zurück.

Sie können [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) verwenden, um zwischen diesen beiden Darstellungen zu konvertieren.

Sie können [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) oder [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) verwenden, um den Bezeichner in eine anzuzeigende Zeichenfolge zu ändern.

Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf OLE32.DLL festgelegt werden, wie im folgenden Beispiel gezeigt:

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[&lt;&gt;ProgID-Schlüssel](-progid--key.md)
</dt> </dl>

 

 




