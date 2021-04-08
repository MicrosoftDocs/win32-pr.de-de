---
title: UI_PKEY_Keytip
description: Bezeichnet die Benutzeroberflächen- \_ pkey- \_ KeyTip-Eigenschaft.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947783"
---
# <a name="ui_pkey_keytip"></a>UI- \_ pkey- \_ KeyTip

Bezeichnet die Benutzeroberflächen- \_ pkey- \_ KeyTip-Eigenschaft.

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

Der Benutzeroberflächen- \_ pkey- \_ KeyTip wird von einer Anwendung verwendet, um den Tastaturbeschleuniger eines Menüband-Steuer Elements abzufragen.

Dieser Eigenschafts Wert ist eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen einschließlich Leerzeichen besteht.

Der Wert von UI \_ pkey \_ KeyTip fungiert als Tastaturbeschleuniger für einen Befehl, es sei denn, dieser Befehl wird über ein Menü Element verfügbar gemacht. In diesem Fall ignoriert das Framework den Benutzeroberflächen- \_ pkey \_ -KeyTip-Wert und verwendet stattdessen ein Zeichen, dem ein kaufmännisches und-Zeichen vorangestellt ist, wie durch [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [UI \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)angegeben. Wenn kein kaufmännisches und von der Bezeichnung " **Command. labeltitle** " oder "UI pkey" angegeben wird \_ \_ , wird kein KeyTip oder keine Tastatur Beschleunigung bereitgestellt.

Die maximale Länge des UI- \_ pkey- \_ KeyTip ist unbegrenzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Eigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. KeyTip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




