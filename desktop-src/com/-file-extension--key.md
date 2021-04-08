---
title: file_extension-Taste
description: Ordnet eine Dateinamenerweiterung einer ProgID zu.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856911"
---
# <a name="file_extension-key"></a><Datei \_ Erweiterung> Schlüssel

Ordnet eine Dateinamenerweiterung einer ProgID zu.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Bemerkungen

Die im Dateinamen-Erweiterungs Schlüssel enthaltenen Informationen werden sowohl von Windows Explorer als auch von dateimonikern verwendet. [**Getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet den Schlüssel für die Dateinamenerweiterung zum Bereitstellen der zugeordneten CLSID.

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**Getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




